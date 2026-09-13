---
navigation:
  order: 20
---

# 4.2 请求与响应

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "购物清单\n- 牛奶\n- 鸡蛋",
  "deviceId": "d_macbook"
}
```

响应（成功）:

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

响应（冲突。返回按 [3.4 的规则](../03-architecture/conflicts.md) 解决后的结果）:

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "购物清单\n- 牛奶\n- 鸡蛋\n>>> d_iphone\n- 面包" }
```
