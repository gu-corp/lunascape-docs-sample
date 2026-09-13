---
navigation:
  order: 30
---

# 2.3 Nachverfolgbarkeit der Anforderungen

Die Anforderungen werden den Elementen der [Architektur](../03-architecture/README.md) und den Endpunkten der [API](../04-api/README.md) zugeordnet. Eine Anforderung ohne Zuordnung gilt als nicht umgesetzt.

```mermaid
flowchart LR
  REQ001[REQ-001 trifft innerhalb von 10 s ein] --> PUSH["/notes/push"]
  REQ002[REQ-002 Senden bei erneuter Verbindung] --> QUEUE[Warteschlange auf dem Gerät]
  REQ003[REQ-003 Konflikterkennung] --> VERSION[Abgleich der Versionsnummer]
  REQ004[REQ-004 automatische Auflösung] --> MERGE[Drei-Wege-Zusammenführung]
  QUEUE --> PUSH
  VERSION --> MERGE
```
