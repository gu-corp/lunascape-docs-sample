---
navigation:
  order: 20
---

# 4.2 Requête et réponse

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Courses\n- Lait\n- Œufs",
  "deviceId": "d_macbook"
}
```

Réponse (succès) :

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Réponse (conflit : le corps renvoyé est le résultat de [la règle de 3.4](../03-architecture/conflicts.md)) :

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Courses\n- Lait\n- Œufs\n>>> d_iphone\n- Pain" }
```
