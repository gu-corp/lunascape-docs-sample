---
navigation:
  order: 20
---

# 4.2 Begäran och svar

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Inköp\n- Mjölk\n- Ägg",
  "deviceId": "d_macbook"
}
```

Svar (lyckat):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Svar (konflikt – texten som returneras är resultatet av [reglerna i 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Inköp\n- Mjölk\n- Ägg\n>>> d_iphone\n- Bröd" }
```
