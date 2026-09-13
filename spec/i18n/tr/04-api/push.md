---
navigation:
  order: 20
---

# 4.2 İstek ve yanıt

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Alışveriş\n- Süt\n- Yumurta",
  "deviceId": "d_macbook"
}
```

Yanıt (başarılı):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Yanıt (çakışma — döndürülen gövde, [3.4'teki kurallar](../03-architecture/conflicts.md) ile çözülen sonuçtur):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Alışveriş\n- Süt\n- Yumurta\n>>> d_iphone\n- Ekmek" }
```
