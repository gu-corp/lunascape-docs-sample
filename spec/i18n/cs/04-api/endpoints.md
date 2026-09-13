---
navigation:
  order: 10
---

# 4.1 Koncové body

| Metoda | Cesta | Účel | Požadavek |
|---|---|---|---|
| POST | `/notes/push` | Odeslat změnu poznámky | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Přijmout změny novější než zadaná verze | REQ-001 |
| DELETE | `/notes/{id}` | Odstranit poznámku (do koše) | REQ-005 |
| POST | `/notes/{id}/restore` | Obnovit poznámku z koše | REQ-005 |
