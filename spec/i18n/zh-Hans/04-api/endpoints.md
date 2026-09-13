---
navigation:
  order: 10
---

# 4.1 端点

| 方法 | 路径 | 用途 | 需求 |
|---|---|---|---|
| POST | `/notes/push` | 发送笔记的变更 | REQ-001、REQ-002 |
| GET | `/notes/pull?since=<version>` | 接收指定版本之后的变更 | REQ-001 |
| DELETE | `/notes/{id}` | 删除笔记（移入回收站） | REQ-005 |
| POST | `/notes/{id}/restore` | 从回收站恢复 | REQ-005 |
