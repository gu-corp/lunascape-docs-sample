---
navigation:
  order: 20
---

# 4.2 अनुरोध और प्रतिक्रिया

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "खरीदारी\n- दूध\n- अंडे",
  "deviceId": "d_macbook"
}
```

प्रतिक्रिया (सफल):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

प्रतिक्रिया (विरोध। [3.4 के नियमों](../03-architecture/conflicts.md) से हल किया गया परिणाम लौटाया जाता है):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "खरीदारी\n- दूध\n- अंडे\n>>> d_iphone\n- ब्रेड" }
```
