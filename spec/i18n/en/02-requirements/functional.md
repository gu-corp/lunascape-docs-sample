---
navigation:
  order: 10
---

# 2.1 Functional requirements

| ID | Requirement | Priority | Verification |
|---|---|---|---|
| REQ-001 | A note created on one device reaches other devices within 10 seconds of reconnecting | Required | Integration test |
| REQ-002 | A note edited offline is sent automatically on reconnection | Required | Integration test |
| REQ-003 | Two updates to the same version are detected as a conflict | Required | Unit test |
| REQ-004 | A conflict is resolved automatically by [the rules in 3.4](../03-architecture/conflicts.md), without losing either side's content | Required | Unit test |
| REQ-005 | A deletion is propagated to other devices, and can be restored from the trash for 30 days | Recommended | Integration test |
| REQ-006 | A device can display the sync status (synced, sending, conflict) | Recommended | Visual inspection |
