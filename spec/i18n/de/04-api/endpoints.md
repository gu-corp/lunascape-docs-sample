---
navigation:
  order: 10
---

# 4.1 Endpunkte

| Methode | Pfad | Zweck | Anforderung |
|---|---|---|---|
| POST | `/notes/push` | Eine Änderung an einer Notiz senden | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Änderungen nach der angegebenen Version empfangen | REQ-001 |
| DELETE | `/notes/{id}` | Eine Notiz löschen (in den Papierkorb) | REQ-005 |
| POST | `/notes/{id}/restore` | Eine Notiz aus dem Papierkorb wiederherstellen | REQ-005 |
