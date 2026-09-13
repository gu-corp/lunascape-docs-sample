---
navigation:
  order: 30
---

# 4.3 Erreurs

| État | Signification | Action du terminal |
|---|---|---|
| 400 | Format de la requête incorrect | Cesser l'envoi et le consigner dans le journal |
| 401 | Jeton non valide | Se réauthentifier |
| 409 | Version non concordante (conflit) | Remplacer par le `body` de la réponse et signaler un conflit |
| 413 | Corps supérieur à 1 Mo | Avertir l'utilisateur et ne pas envoyer |
| 429 | Trop de requêtes | Attendre le nombre de secondes indiqué par `Retry-After`, puis renvoyer |
| 5xx | Défaillance du serveur | Renvoyer avec un délai exponentiel (5 fois au maximum) |
