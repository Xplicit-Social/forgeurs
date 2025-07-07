<!--
{
  "id": "1_[Mission]_[Modèle]",
  "secteur": "communication",
  "xplt": 0,
  "statut": "ouverte"
}
-->

# Mission 1 — Modèle de mission
Cette mission sert de **référence officielle** pour structurer toutes les missions de La Forge.

## Objectif
Expliquer **comment formater et gérer une mission dans La Forge** :
- Fichiers nécessaires
- Fonctionnement des votes et discussions
- Attribution des récompenses XPLT

## Structure requise
```css<code>
mission/
├── mission.md ← description textuelle de la mission
├── votes.json ← votes utilisateurs
├── xplt.json ← votes utilisateurs
└── chat.json ← discussion communautaire avec payload inline dans la balise </code>```

## Processus de mission
1️⃣  **Mission créée par La Forge** dans le dépôt  
2️⃣  Discussion via le **chat intégré** (`chat.json`)  
3️⃣  Votes enregistrés dans **`meta.json`**  
4️⃣  Réalisation par **les Initiés**  
5️⃣  Attribution de la **récompense XPLT** dans `meta.json`  
6️⃣  Mission **close et archivée**, consultable publiquement

## Récompense
Une mission peut inclure :
- **Bounty XPLT fixe** selon la complexité
- Répartition entre plusieurs contributeurs par vote
- Bonus si la mission est validée sans correction

## Participation
**Pas de propositions externes.**  
Seules les missions créées par **La Forge** sont valides.


## Discussion
Les discussions se font dans le **chat intégré**.  
Pour proposer du code, utilisez des blocs :

```css<code>
votre code ici
</code>```

Bonne chance si vous l'acceptez 
