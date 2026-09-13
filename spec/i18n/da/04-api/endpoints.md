---
navigation:
  order: 10
---

# 4.1 Endepunkter

| Metode | Sti | Formål | Krav |
|---|---|---|---|
| POST | `/notes/push` | Send en ændring til en note | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Modtag ændringer efter den angivne version | REQ-001 |
| DELETE | `/notes/{id}` | Slet en note (til papirkurven) | REQ-005 |
| POST | `/notes/{id}/restore` | Gendan en note fra papirkurven | REQ-005 |
