---
navigation:
  order: 20
---

# 4.2 Richiesta e risposta

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Spesa\n- Latte\n- Uova",
  "deviceId": "d_macbook"
}
```

Risposta (successo):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Risposta (conflitto: viene restituito il risultato ottenuto applicando [le regole di 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Spesa\n- Latte\n- Uova\n>>> d_iphone\n- Pane" }
```
