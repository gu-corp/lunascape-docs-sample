---
navigation:
  order: 20
---

# 4.2 Forespørsel og svar

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Handleliste\n- Melk\n- Egg",
  "deviceId": "d_macbook"
}
```

Svar (vellykket):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Svar (konflikt – returnerer resultatet av [reglene i 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Handleliste\n- Melk\n- Egg\n>>> d_iphone\n- Brød" }
```
