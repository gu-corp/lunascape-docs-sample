---
navigation:
  order: 20
---

# 4.2 Pyyntö ja vastaus

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Ostokset\n- Maito\n- Kananmunat",
  "deviceId": "d_macbook"
}
```

Vastaus (onnistunut):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Vastaus (ristiriita – palautetaan tulos, joka on ratkaistu [kohdan 3.4 sääntöjen](../03-architecture/conflicts.md) mukaisesti):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Ostokset\n- Maito\n- Kananmunat\n>>> d_iphone\n- Leipä" }
```
