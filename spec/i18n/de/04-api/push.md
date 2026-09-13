---
navigation:
  order: 20
---

# 4.2 Anfrage und Antwort

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Einkaufen\n- Milch\n- Eier",
  "deviceId": "d_macbook"
}
```

Antwort (Erfolg):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Antwort (Konflikt – zurückgegeben wird das Ergebnis [der Regeln in 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Einkaufen\n- Milch\n- Eier\n>>> d_iphone\n- Brot" }
```
