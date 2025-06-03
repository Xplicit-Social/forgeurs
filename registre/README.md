// interne.ts : opérations manuelles réservées au Conseil

import { Hono } from 'hono'
import { readFile, writeFile, appendFile, mkdir } from 'fs/promises'
import { join } from 'path'
import { formatISO } from 'date-fns'

const interne = new Hono()
const REGISTRE_PATH = './registre'

function withCouncilAuth(secret) {
  return async (c, next) => {
    const incoming = c.req.header('authorization') || ''
    if (incoming !== `Bearer ${secret}`) return c.text('Forbidden - Conseil only', 403)
    return next()
  }
}

async function appendLog(entry) {
  const now = new Date()
  const date = now.toISOString().split('T')[0]
  const logPath = join(REGISTRE_PATH, 'logs')
  const logFile = join(logPath, `tx-${date}.jsonl`)
  const ts = formatISO(now)

  await mkdir(logPath, { recursive: true })
  const fullEntry = { ts, ...entry }
  await appendFile(logFile, JSON.stringify(fullEntry) + '\n')
}

interne.use('*', withCouncilAuth(process.env.COUNCIL_SECRET || 'council'))

// Exemple : redistribution manuelle depuis la réserve
interne.post('/council/reward', async c => {
  const { to, amount, reason } = await c.req.json()
  const path = join(REGISTRE_PATH, 'balances.json')
  const balances = JSON.parse(await readFile(path, 'utf-8'))

  balances[to] = (balances[to] || 0) + amount
  balances.reserve = (balances.reserve || 0) - amount

  await writeFile(path, JSON.stringify(balances, null, 2))
  await appendLog({ action: 'transfer', from: 'reserve', to, amount, reason })

  return c.json({ status: 'ok', to, amount, reason })
})

export { interne }
