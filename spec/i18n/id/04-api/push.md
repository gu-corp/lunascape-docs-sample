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
  "body": "Belanja\n- Susu\n- Telur",
  "deviceId": "d_macbook"
}
```

Respons (berhasil):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Respons (konflik. Yang dikembalikan adalah hasil penyelesaian menurut [aturan pada 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Belanja\n- Susu\n- Telur\n>>> d_iphone\n- Roti" }
```
