---
navigation:
  order: 20
---

# 4.2 Cerere și răspuns

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Cumpărături\n- Lapte\n- Ouă",
  "deviceId": "d_macbook"
}
```

Răspuns (succes):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Răspuns (conflict — se returnează rezultatul obținut prin [regulile din 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Cumpărături\n- Lapte\n- Ouă\n>>> d_iphone\n- Pâine" }
```
