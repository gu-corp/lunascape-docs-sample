---
navigation:
  order: 10
---

# 4.1 Eindpunten

| Methode | Pad | Doel | Vereiste |
|---|---|---|---|
| POST | `/notes/push` | Een wijziging in een notitie verzenden | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Wijzigingen na de opgegeven versie ontvangen | REQ-001 |
| DELETE | `/notes/{id}` | Een notitie verwijderen (naar de Prullenbak) | REQ-005 |
| POST | `/notes/{id}/restore` | Een notitie terugzetten uit de Prullenbak | REQ-005 |
