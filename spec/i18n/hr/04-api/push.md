---
navigation:
  order: 20
---

# 4.2 Zahtjev i odgovor

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Kupovina\n- Mlijeko\n- Jaja",
  "deviceId": "d_macbook"
}
```

Odgovor (uspjeh):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Odgovor (sukob — vraća se rezultat razrješenja prema [pravilima iz 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Kupovina\n- Mlijeko\n- Jaja\n>>> d_iphone\n- Kruh" }
```
