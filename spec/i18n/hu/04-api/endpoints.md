---
navigation:
  order: 10
---

# 4.1 Végpontok

| Metódus | Útvonal | Cél | Követelmény |
|---|---|---|---|
| POST | `/notes/push` | Jegyzet módosításának elküldése | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | A megadott verzió utáni módosítások fogadása | REQ-001 |
| DELETE | `/notes/{id}` | Jegyzet törlése (a Kukába) | REQ-005 |
| POST | `/notes/{id}/restore` | Jegyzet visszaállítása a Kukából | REQ-005 |
