---
navigation:
  order: 20
---

# 4.2 Yêu cầu và phản hồi

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Mua sắm\n- Sữa\n- Trứng",
  "deviceId": "d_macbook"
}
```

Phản hồi (thành công):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Phản hồi (xung đột. Trả về kết quả đã được giải quyết theo [quy tắc ở mục 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Mua sắm\n- Sữa\n- Trứng\n>>> d_iphone\n- Bánh mì" }
```
