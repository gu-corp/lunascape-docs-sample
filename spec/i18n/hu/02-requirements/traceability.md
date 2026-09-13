---
navigation:
  order: 30
---

# 2.3 A követelmények nyomon követése

A követelményeket hozzá kell rendelni [a felépítés](../03-architecture/README.md) egyes elemeihez és [az API](../04-api/README.md) egyes végpontjaihoz. A hozzárendelés nélküli követelmény megvalósítatlannak számít.

```mermaid
flowchart LR
  REQ001[REQ-001 10 másodpercen belül megérkezik] --> PUSH["/notes/push"]
  REQ002[REQ-002 újracsatlakozáskor elküldve] --> QUEUE[Eszközoldali várósor]
  REQ003[REQ-003 ütközés észlelése] --> VERSION[Verziószám egyeztetése]
  REQ004[REQ-004 automatikus feloldás] --> MERGE[Háromutas összefésülés]
  QUEUE --> PUSH
  VERSION --> MERGE
```
