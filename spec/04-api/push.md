---
navigation:
  order: 20
---

# 4.2 要求と応答

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "買い物\n- 牛乳\n- 卵",
  "deviceId": "d_macbook"
}
```

応答（成功）:

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

応答（競合。[3.4 の規則](../03-architecture/conflicts.md) で解決した結果を返す）:

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "買い物\n- 牛乳\n- 卵\n>>> d_iphone\n- パン" }
```
