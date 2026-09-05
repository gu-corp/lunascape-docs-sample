---
navigation:
  order: 40
---

# 4. API

すべてのエンドポイントは `https://api.orbit.example/v1` を基点とし、`Authorization: Bearer <token>` を要求する。本文は JSON（UTF-8）とする。

## 4.1 エンドポイント

| メソッド | パス | 目的 | 要件 |
|---|---|---|---|
| POST | `/notes/push` | ノートの変更を送る | REQ-001、REQ-002 |
| GET | `/notes/pull?since=<version>` | 指定した版より後の変更を受け取る | REQ-001 |
| DELETE | `/notes/{id}` | ノートを削除する（ごみ箱へ） | REQ-005 |
| POST | `/notes/{id}/restore` | ごみ箱から戻す | REQ-005 |

## 4.2 要求と応答

### POST /notes/push

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

応答（競合。3.4 の規則で解決した結果を返す）:

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "買い物\n- 牛乳\n- 卵\n>>> d_iphone\n- パン" }
```

## 4.3 エラー

| 状態 | 意味 | 端末の対処 |
|---|---|---|
| 400 | 要求の形式が不正 | 送信をやめ、ログに残す |
| 401 | トークンが無効 | 再認証する |
| 409 | 版の不一致（競合） | 応答の `body` で置き換え、競合ありと表示する |
| 413 | 本文が 1 MB を超える | 利用者に知らせ、送信しない |
| 429 | 要求が多すぎる | `Retry-After` の秒数だけ待って再送する |
| 5xx | サーバーの障害 | 指数バックオフで再送する（最大 5 回） |
