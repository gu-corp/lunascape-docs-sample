---
navigation:
  order: 10
---

# 4.1 Points de terminaison

| Méthode | Chemin | Objet | Exigence |
|---|---|---|---|
| POST | `/notes/push` | Envoyer une modification d'une note | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Recevoir les modifications postérieures à la version indiquée | REQ-001 |
| DELETE | `/notes/{id}` | Supprimer une note (vers la corbeille) | REQ-005 |
| POST | `/notes/{id}/restore` | Restaurer une note depuis la corbeille | REQ-005 |
