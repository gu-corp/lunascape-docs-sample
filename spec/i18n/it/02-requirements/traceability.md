---
navigation:
  order: 30
---

# 2.3 Tracciabilità dei requisiti

I requisiti sono associati a ciascun elemento dell'[architettura](../03-architecture/README.md) e a ciascun endpoint dell'[API](../04-api/README.md). Un requisito privo di associazione è considerato non implementato.

```mermaid
flowchart LR
  REQ001[REQ-001 recapito entro 10 secondi] --> PUSH["/notes/push"]
  REQ002[REQ-002 invio alla riconnessione] --> QUEUE[Coda sul dispositivo]
  REQ003[REQ-003 rilevamento dei conflitti] --> VERSION[Confronto dei numeri di versione]
  REQ004[REQ-004 risoluzione automatica] --> MERGE[Merge a tre vie]
  QUEUE --> PUSH
  VERSION --> MERGE
```
