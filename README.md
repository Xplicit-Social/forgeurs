# 🧠 XPLICIT Forge — Système de Missions Collaboratives

Bienvenue dans la **Forge** de XPLICIT.  
Ici, chaque utilisateur peut **contribuer, voter, être récompensé**.  
C’est un système décentralisé de co-développement, basé sur la méritocratie et la transparence.

---

## 🧩 Concepts Clés

### 🔨 Mission

Une **mission** est une unité de travail ciblée : refonte, ajout de fonctionnalité, debug, spec, etc.

Chaque mission vit dans un dossier unique :

missions/
└── 0001-nom-de-la-mission/


### 👥 Contributeurs

Chaque membre peut participer :
- en **postant sa propre version de code**
- en **discutant** via le `chat.log`
- en **votant** pour la meilleure proposition
- en recevant des **XPLT (points)** si sa solution est retenue

---

## 📂 Structure d’une mission

0001-nom-de-la-mission/
├── mission.md ← Objectif, Contexte, Fichiers cibles
├── payload/ ← Fichiers originaux (référence)
├── usercode/ ← Propositions individuelles
│ └── <pseudo>/ ← Ton dossier personnel
│ └── tes fichiers.ts
├── chat.log ← Historique des échanges
├── votes.json ← Système de validation
├── xplt-rewards.json ← Répartition des gains
└── users.json ← Infos participants (role, date)


---

## 🚀 Comment participer

### 1. Choisis une mission dans `/missions`

### 2. Lis le `mission.md`

Comprends bien ce qui est demandé, les contraintes, les fichiers à modifier.

### 3. Dépose ta solution

Utilise l’interface **commander** ou l’API :

POST /missions/:missionId/usercode/:pseudo/upload


👉 Les fichiers sont enregistrés dans :  
`/missions/<missionId>/usercode/<pseudo>/`

### 4. Attends ou déclenche un **vote**

Une fois plusieurs versions soumises, un vote est ouvert dans `votes.json`.

---

## 🏅 Récompenses en $XPLT

Si ta version est retenue, tu gagnes :

- 🔹 des **points XPLT**
- 🔹 une **reconnaissance publique**
- 🔹 un rang ou badge dans le réseau (si activé)

> Les récompenses sont définies manuellement ou automatiquement dans `xplt-rewards.json`

---

## 🛑 Règles de base

- Ne jamais modifier `payload/`
- Ne jamais poster de code dans `mission.md`
- Utiliser **exclusivement `usercode/<pseudo>/`**
- Pas de fichier externe ni dépendance non autorisée
- Code lisible, optimisé, sans commentaires inutiles

---

## 🧠 Pourquoi ce système ?

- ✅ Encourager les développeurs à proposer des solutions concurrentes
- ✅ Favoriser les meilleurs sans favoritisme
- ✅ Récompenser le mérite réel, pas la visibilité
- ✅ Accélérer la production via missions ciblées

---

## 🔐 Authentification & Sécurité

- Toutes les requêtes passent par **mTLS + JWT**
- Chaque utilisateur est identifié de manière **cryptographique**
- L'historique est 100% traçable via Git

---

## 📌 Statuts possibles des missions

| Statut     | Signification                              |
|------------|---------------------------------------------|
| 🟢 Ouverte  | Acceptant les contributions                 |
| 🟡 En cours | Contributions reçues, vote à venir          |
| 🔴 Fermée   | Une version a été retenue et intégrée       |