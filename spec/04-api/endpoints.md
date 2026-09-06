---
navigation:
  order: 10
---

# 4.1 エンドポイント

| メソッド | パス | 目的 | 要件 |
|---|---|---|---|
| POST | `/notes/push` | ノートの変更を送る | REQ-001、REQ-002 |
| GET | `/notes/pull?since=<version>` | 指定した版より後の変更を受け取る | REQ-001 |
| DELETE | `/notes/{id}` | ノートを削除する（ごみ箱へ） | REQ-005 |
| POST | `/notes/{id}/restore` | ごみ箱から戻す | REQ-005 |
