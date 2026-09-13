---
navigation:
  order: 10
---

# 4.1 Uç noktalar

| Yöntem | Yol | Amaç | Gereksinim |
|---|---|---|---|
| POST | `/notes/push` | Not değişikliklerini gönderir | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Belirtilen sürümden sonraki değişiklikleri alır | REQ-001 |
| DELETE | `/notes/{id}` | Notu siler (çöp kutusuna taşır) | REQ-005 |
| POST | `/notes/{id}/restore` | Notu çöp kutusundan geri getirir | REQ-005 |
