---
navigation:
  order: 30
---

# 2.3 Traceerbaarheid van eisen

Eisen worden gekoppeld aan de elementen van [de architectuur](../03-architecture/README.md) en aan de eindpunten van [de API](../04-api/README.md). Een eis zonder koppeling geldt als niet geïmplementeerd.

```mermaid
flowchart LR
  REQ001[REQ-001 komt binnen 10 s aan] --> PUSH["/notes/push"]
  REQ002[REQ-002 verzonden bij herverbinding] --> QUEUE[Wachtrij op het apparaat]
  REQ003[REQ-003 conflictdetectie] --> VERSION[Controle van versienummer]
  REQ004[REQ-004 automatische oplossing] --> MERGE[Driewegsamenvoeging]
  QUEUE --> PUSH
  VERSION --> MERGE
```
