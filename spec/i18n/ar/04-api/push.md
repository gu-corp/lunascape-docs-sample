---
navigation:
  order: 20
---

# 4.2 الطلب والاستجابة

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "التسوّق\n- حليب\n- بيض",
  "deviceId": "d_macbook"
}
```

الاستجابة (نجاح):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

الاستجابة (تعارض. يُعاد الناتج بعد الحل وفق [القواعد في 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "التسوّق\n- حليب\n- بيض\n>>> d_iphone\n- خبز" }
```
