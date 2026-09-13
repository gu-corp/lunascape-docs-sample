---
navigation:
  order: 20
---

# 4.2 בקשה ותגובה

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "קניות\n- חלב\n- ביצים",
  "deviceId": "d_macbook"
}
```

תגובה (הצלחה):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

תגובה (התנגשות — מוחזרת התוצאה שנפתרה לפי [הכללים שב־3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "קניות\n- חלב\n- ביצים\n>>> d_iphone\n- לחם" }
```
