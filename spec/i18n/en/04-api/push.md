---
navigation:
  order: 20
---

# 4.2 Request and response

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Groceries\n- Milk\n- Eggs",
  "deviceId": "d_macbook"
}
```

Response (success):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Response (conflict — the body returned is the result of [the rules in 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Groceries\n- Milk\n- Eggs\n>>> d_iphone\n- Bread" }
```
