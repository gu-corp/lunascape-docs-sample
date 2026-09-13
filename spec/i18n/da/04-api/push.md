---
navigation:
  order: 20
---

# 4.2 Forespørgsel og svar

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Indkøb\n- Mælk\n- Æg",
  "deviceId": "d_macbook"
}
```

Svar (vellykket):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Svar (konflikt — den returnerede tekst er resultatet af [reglerne i 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Indkøb\n- Mælk\n- Æg\n>>> d_iphone\n- Brød" }
```
