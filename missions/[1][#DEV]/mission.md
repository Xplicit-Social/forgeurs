<!--
{
  "id": "0001-modele-mission",
  "secteur": "documentation",
  "niveau": "débutant",
  "votes": 5
}
-->

# 📘 Mission 0001 — Modèle de mission

Ce fichier sert de **référence officielle** pour structurer toutes les missions de La Forge.  
Il définit les champs obligatoires, les fichiers attendus, et le déroulement complet d’une mission communautaire.

---

## 📁 Structure standard d’une mission



---

missions/
└── <id>-slug/
├── mission.md ← description structurée de la mission (obligatoire)
├── payload.md ← liste des fichiers techniques liés (liens proxy)
├── votes.json ← votes communautaires (optionnel)
├── rewards.json ← récompense prévue ou attribuée
└── users.json ← forgeurs autorisés à intervenir

---

## 🎯 Objectif

Chaque mission a un objectif unique, explicite et actionnable.  
Il peut s’agir de :

- créer un nouveau module ou outil,
- corriger un problème précis,
- documenter une fonctionnalité,
- auditer ou refactorer un composant existant.

---

## 🧱 Contenu minimal du `mission.md`

| Champ | Détail attendu |
|-------|----------------|
| `Objectif` | Ce que doit accomplir la mission |
| `Contexte` | Pourquoi cette mission existe, d’où vient le besoin |
| `Contraintes` | Outils autorisés, interdits, exigences techniques |
| `Livrables` | Fichiers attendus, preuves, tests |
| `Récompense` | Montant XPLT attribué ou en discussion |
| `Processus` | Comment participer, voter, proposer une solution |

---

## 🧩 Description des fichiers associés

- [`payload.md`](/api/gitlab/proxy?path=missions/0001-modele-mission/payload.md)  
  Liste et description des fichiers techniques utiles à cette mission (schémas, specs, exemples, etc.)

- [`votes.json`](/api/gitlab/proxy?path=missions/0001-modele-mission/votes.json)  
  Historique des votes et positions exprimées par les Forgeurs.

- [`xplt-rewards.json`](/api/gitlab/proxy?path=missions/0001-modele-mission/xplt-rewards.json)  
  Répartition de la récompense prévue ou finale (en XPLT).

- [`users.json`](/api/gitlab/proxy?path=missions/0001-modele-mission/users.json)  
  Pseudos ou empreintes des forgeurs autorisés à interagir (édition, vote, validation).

---

## 🛠 Déroulement d'une mission

1. 🧱 **Mission proposée par La Forge**  
   → via dépôt Git `missions/<id>/`

2. 💬 **Discussion communautaire**  
   → via chat intégré à la page de mission

3. 🧠 **Votes ouverts dans `votes.json`**  
   → chaque forgeur s’exprime avec justification

4. 🛠 **Merge Requests autorisées**  
   → si la mission est ouverte à contributions

5. ✅ **Validation + récompense**  
   → via commit dans `xplt-rewards.json`

---

## 🔐 Règle actuelle

Aucune mission ne peut être soumise librement.  
👉 **Elles sont exclusivement proposées par l'équipe** au lancement du projet.

---

## 🔗 Accès rapide

- [Lire le `payload.md`](payload.md)
- [Voir les votes](votes.json)
- [Récompense prévue](xplt-rewards.json)

---

Ce fichier fait office de **gabarit de référence**.  
Toute mission future doit en dériver ou s’y conformer.
