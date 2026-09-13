---
navigation:
  order: 10
---

# 4.1 端點

| 方法 | 路徑 | 用途 | 需求 |
|---|---|---|---|
| POST | `/notes/push` | 傳送筆記的變更 | REQ-001、REQ-002 |
| GET | `/notes/pull?since=<version>` | 接收指定版本之後的變更 | REQ-001 |
| DELETE | `/notes/{id}` | 刪除筆記（移至垃圾桶） | REQ-005 |
| POST | `/notes/{id}/restore` | 從垃圾桶還原 | REQ-005 |
