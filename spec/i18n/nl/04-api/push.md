---
navigation:
  order: 20
---

# 4.2 Verzoek en antwoord

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Boodschappen\n- Melk\n- Eieren",
  "deviceId": "d_macbook"
}
```

Antwoord (geslaagd):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Antwoord (conflict — het resultaat van [de regels in 3.4](../03-architecture/conflicts.md) wordt teruggegeven):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Boodschappen\n- Melk\n- Eieren\n>>> d_iphone\n- Brood" }
```
