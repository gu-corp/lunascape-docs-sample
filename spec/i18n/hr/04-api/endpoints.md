---
navigation:
  order: 10
---

# 4.1 Krajnje točke

| Metoda | Putanja | Svrha | Zahtjev |
|---|---|---|---|
| POST | `/notes/push` | Slanje promjene bilješke | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Primanje promjena nakon navedene verzije | REQ-001 |
| DELETE | `/notes/{id}` | Brisanje bilješke (u koš za smeće) | REQ-005 |
| POST | `/notes/{id}/restore` | Vraćanje bilješke iz koša za smeće | REQ-005 |
