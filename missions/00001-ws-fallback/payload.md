<!--
{
  "format": "payload.md",
  "version": 1
}
-->

# 🔗 Fichiers techniques liés à la mission

Cette page recense les **fichiers techniques** nécessaires à la compréhension, l'implémentation ou la validation de cette mission.

---

## 📐 Schémas Zod

- [`schema.zod.ts`](/api/gitlab/proxy?path=missions/0001-modele-mission/schema.zod.ts)  
  Décrit les structures de données attendues dans les échanges JSON (API ou WebSocket).

---

## 📦 Spécifications API

- [`api-spec.json`](/api/gitlab/proxy?path=missions/0001-modele-mission/api-spec.json)  
  Spécification brutale ou partielle de l’API utilisée (OpenAPI ou format custom).

---

## 🧪 Tests ou mocks (optionnel)

- [`examples/request.json`](/api/gitlab/proxy?path=missions/0001-modele-mission/examples/request.json)  
  Exemple de requête valide utilisée dans un scénario type.

- [`examples/response.json`](/api/gitlab/proxy?path=missions/0001-modele-mission/examples/response.json)  
  Réponse attendue, à valider via test unitaire ou endpoint simulé.

---

## 🛠 Autres références utiles

- [`legacy.ts`](/api/gitlab/proxy?path=missions/0001-modele-mission/legacy.ts)  
  Ancienne implémentation (à corriger, adapter ou remplacer).

---

## ✍️ Comment ajouter un nouveau fichier technique ?

1. Crée le fichier dans le dossier de la mission sur ton fork
2. Commit avec un nom explicite
3. Ajoute une entrée ici en suivant la syntaxe `[nom](url)`
4. Fais une merge request

---

💡 Les liens sont automatiquement redirigés vers le proxy `/api/gitlab/proxy?path=...` pour éviter les erreurs CORS.
