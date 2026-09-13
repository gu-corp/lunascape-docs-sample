---
navigation:
  order: 20
---

# 4.2 Kérés és válasz

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Bevásárlás\n- Tej\n- Tojás",
  "deviceId": "d_macbook"
}
```

Válasz (sikeres):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Válasz (ütközés – a visszaadott törzs [a 3.4 szabályai](../03-architecture/conflicts.md) szerinti feloldás eredménye):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Bevásárlás\n- Tej\n- Tojás\n>>> d_iphone\n- Kenyér" }
```
