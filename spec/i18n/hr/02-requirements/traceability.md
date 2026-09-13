---
navigation:
  order: 30
---

# 2.3 Praćenje zahtjeva

Zahtjevi se pridružuju elementima [arhitekture](../03-architecture/README.md) i krajnjim točkama [API-ja](../04-api/README.md). Zahtjev bez pridruženog elementa smatra se neimplementiranim.

```mermaid
flowchart LR
  REQ001[REQ-001 stiže unutar 10 s] --> PUSH["/notes/push"]
  REQ002[REQ-002 šalje se pri ponovnom povezivanju] --> QUEUE[Red čekanja na uređaju]
  REQ003[REQ-003 otkrivanje sukoba] --> VERSION[Provjera broja verzije]
  REQ004[REQ-004 automatsko razrješavanje] --> MERGE[Tronačinsko spajanje]
  QUEUE --> PUSH
  VERSION --> MERGE
```
