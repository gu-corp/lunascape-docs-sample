---
navigation:
  order: 30
---

# 2.3 Traceability

Requirements are mapped to the elements of [the architecture](../03-architecture/README.md) and the endpoints of [the API](../04-api/README.md). A requirement with no mapping is treated as unimplemented.

```mermaid
flowchart LR
  REQ001[REQ-001 arrives within 10s] --> PUSH["/notes/push"]
  REQ002[REQ-002 sent on reconnect] --> QUEUE[Device-side queue]
  REQ003[REQ-003 conflict detection] --> VERSION[Version check]
  REQ004[REQ-004 automatic resolution] --> MERGE[Three-way merge]
  QUEUE --> PUSH
  VERSION --> MERGE
```
