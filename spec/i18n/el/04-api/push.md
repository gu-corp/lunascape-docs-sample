---
navigation:
  order: 20
---

# 4.2 Αίτημα και απόκριση

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Ψώνια\n- Γάλα\n- Αυγά",
  "deviceId": "d_macbook"
}
```

Απόκριση (επιτυχία):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Απόκριση (διένεξη· επιστρέφεται το αποτέλεσμα της επίλυσης με [τους κανόνες της ενότητας 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Ψώνια\n- Γάλα\n- Αυγά\n>>> d_iphone\n- Ψωμί" }
```
