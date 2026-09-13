---
navigation:
  order: 10
---

# 4.1 Slutpunkter

| Metod | Sökväg | Syfte | Krav |
|---|---|---|---|
| POST | `/notes/push` | Skicka en ändring av en anteckning | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Ta emot ändringar efter den angivna versionen | REQ-001 |
| DELETE | `/notes/{id}` | Ta bort en anteckning (till papperskorgen) | REQ-005 |
| POST | `/notes/{id}/restore` | Återställa en anteckning från papperskorgen | REQ-005 |
