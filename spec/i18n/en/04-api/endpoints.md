---
navigation:
  order: 10
---

# 4.1 Endpoints

| Method | Path | Purpose | Requirement |
|---|---|---|---|
| POST | `/notes/push` | Send a change to a note | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Receive changes after the given version | REQ-001 |
| DELETE | `/notes/{id}` | Delete a note (to the trash) | REQ-005 |
| POST | `/notes/{id}/restore` | Restore a note from the trash | REQ-005 |
