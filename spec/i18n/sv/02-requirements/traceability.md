---
navigation:
  order: 30
---

# 2.3 Spårbarhet av krav

Kraven kopplas till elementen i [arkitekturen](../03-architecture/README.md) och till slutpunkterna i [API:et](../04-api/README.md). Ett krav utan koppling betraktas som ej implementerat.

```mermaid
flowchart LR
  REQ001[REQ-001 kommer fram inom 10 s] --> PUSH["/notes/push"]
  REQ002[REQ-002 skickas vid återanslutning] --> QUEUE[Kö på enheten]
  REQ003[REQ-003 konfliktidentifiering] --> VERSION[Kontroll av versionsnummer]
  REQ004[REQ-004 automatisk lösning] --> MERGE[Trevägssammanslagning]
  QUEUE --> PUSH
  VERSION --> MERGE
```
