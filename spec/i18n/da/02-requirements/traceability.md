---
navigation:
  order: 30
---

# 2.3 Sporbarhed

Krav knyttes til de enkelte elementer i [arkitekturen](../03-architecture/README.md) og til de enkelte endepunkter i [API'et](../04-api/README.md). Et krav uden en sådan tilknytning regnes som ikke implementeret.

```mermaid
flowchart LR
  REQ001[REQ-001 når frem inden for 10 sekunder] --> PUSH["/notes/push"]
  REQ002[REQ-002 sendes ved gentilslutning] --> QUEUE[Kø på enheden]
  REQ003[REQ-003 registrering af konflikter] --> VERSION[Kontrol af versionsnummer]
  REQ004[REQ-004 automatisk løsning] --> MERGE[Trevejsfletning]
  QUEUE --> PUSH
  VERSION --> MERGE
```
