---
navigation:
  order: 10
---

# 4.1 Punkty końcowe

| Metoda | Ścieżka | Cel | Wymaganie |
|---|---|---|---|
| POST | `/notes/push` | Wysyła zmianę w notatce | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Odbiera zmiany nowsze niż podana wersja | REQ-001 |
| DELETE | `/notes/{id}` | Usuwa notatkę (do kosza) | REQ-005 |
| POST | `/notes/{id}/restore` | Przywraca notatkę z kosza | REQ-005 |
