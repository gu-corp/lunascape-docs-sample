---
navigation:
  order: 20
---

# 4.2 Požadavek a odpověď

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Nákup\n- Mléko\n- Vejce",
  "deviceId": "d_macbook"
}
```

Odpověď (úspěch):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Odpověď (konflikt – vrací se výsledek vyřešený podle [pravidel v 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Nákup\n- Mléko\n- Vejce\n>>> d_iphone\n- Chléb" }
```
