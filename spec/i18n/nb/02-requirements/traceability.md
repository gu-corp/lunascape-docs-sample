---
navigation:
  order: 30
---

# 2.3 Sporing av krav

Kravene knyttes til elementene i [arkitekturen](../03-architecture/README.md) og til endepunktene i [API-et](../04-api/README.md). Et krav uten kobling regnes som ikke implementert.

```mermaid
flowchart LR
  REQ001[REQ-001 kommer frem innen 10 sekunder] --> PUSH["/notes/push"]
  REQ002[REQ-002 sendes ved gjenoppkobling] --> QUEUE[Kø på enheten]
  REQ003[REQ-003 oppdaging av konflikt] --> VERSION[Kontroll av versjonsnummer]
  REQ004[REQ-004 automatisk løsning] --> MERGE[Treveis fletting]
  QUEUE --> PUSH
  VERSION --> MERGE
```
