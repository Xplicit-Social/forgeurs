<!--
{
 "statut": "🟩 Ouverte",
  "id": "1-modele-mission",
  "secteur": "Dévellopement",
  "xplt": 10
}
-->

# 🪐 Mission 1 — Modèle de mission

Cette mission sert de **référence officielle** pour structurer toutes les missions de La Forge.

---

## 🎯 Objectif

Expliquer **comment formater et gérer une mission dans La Forge** :
- Fichiers nécessaires
- Fonctionnement des votes et discussions
- Attribution des récompenses XPLT

---

## 📁 Structure requise

mission/
├── mission.md ← description textuelle de la mission
├── meta.json ← votes, utilisateurs, XPLT
└── chat.json ← discussion communautaire avec payload inline en <code>

---

## ⚙️ Processus de mission

1️⃣ **Mission créée par La Forge** dans le dépôt  
2️⃣ Discussion via le **chat intégré** (`chat.json`)  
3️⃣ Votes enregistrés dans **`meta.json`**  
4️⃣ Réalisation par **les Initiés**  
5️⃣ Attribution de la **récompense XPLT** dans `meta.json`  
6️⃣ Mission **close et archivée**, consultable publiquement

---

## 💰 Récompense

Une mission peut inclure :
- **Bounty XPLT fixe** selon la complexité
- Répartition entre plusieurs contributeurs par vote
- Bonus si la mission est validée sans correction

---

## 👥 Participation

🚫 **Pas de propositions externes.**  
✅ Seules les missions créées par **La Forge** sont valides.

---

## 💬 Discussion

Les discussions se font dans le **chat intégré**.  
Pour proposer du code, utilisez des blocs :

```html
<code>
votre code ici
</code>

📄 meta.json

{
  "votes": [
    {
      "user": "fond-alpha",
      "vote": "yes",
      "comment": "Mission de référence validée."
    }
  ],
  "users": ["init-ali", "forg-liu"],
  "xplt": {
    "bounty": 100,
    "distribution": []
  }
}
