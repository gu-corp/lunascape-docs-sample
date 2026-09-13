---
navigation:
  order: 20
---

# 4.2 要求與回應

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "購物\n- 牛奶\n- 雞蛋",
  "deviceId": "d_macbook"
}
```

回應（成功）：

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

回應（衝突。回傳依 [3.4 的規則](../03-architecture/conflicts.md) 解決後的結果）：

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "購物\n- 牛奶\n- 雞蛋\n>>> d_iphone\n- 麵包" }
```
