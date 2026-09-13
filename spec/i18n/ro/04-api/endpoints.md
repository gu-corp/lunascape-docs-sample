---
navigation:
  order: 10
---

# 4.1 Puncte finale

| Metodă | Cale | Scop | Cerință |
|---|---|---|---|
| POST | `/notes/push` | Trimite modificările unei note | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Primește modificările ulterioare versiunii indicate | REQ-001 |
| DELETE | `/notes/{id}` | Șterge o notă (în coșul de gunoi) | REQ-005 |
| POST | `/notes/{id}/restore` | Restaurează o notă din coșul de gunoi | REQ-005 |
