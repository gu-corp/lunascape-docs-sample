---
navigation:
  order: 10
---

# 4.1 Endepunkter

| Metode | Sti | Formål | Krav |
|---|---|---|---|
| POST | `/notes/push` | Sende en endring i et notat | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Motta endringer etter den angitte versjonen | REQ-001 |
| DELETE | `/notes/{id}` | Slette et notat (til papirkurven) | REQ-005 |
| POST | `/notes/{id}/restore` | Gjenopprette et notat fra papirkurven | REQ-005 |
