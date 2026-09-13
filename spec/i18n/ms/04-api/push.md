---
navigation:
  order: 20
---

# 4.2 Permintaan dan respons

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Barangan runcit\n- Susu\n- Telur",
  "deviceId": "d_macbook"
}
```

Respons (berjaya):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Respons (konflik — hasil yang diselesaikan mengikut [peraturan dalam 3.4](../03-architecture/conflicts.md) dikembalikan):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Barangan runcit\n- Susu\n- Telur\n>>> d_iphone\n- Roti" }
```
