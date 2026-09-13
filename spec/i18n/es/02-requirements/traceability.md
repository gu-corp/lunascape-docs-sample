---
navigation:
  order: 30
---

# 2.3 Trazabilidad de los requisitos

Los requisitos se corresponden con cada elemento de [la arquitectura](../03-architecture/README.md) y con cada endpoint de [la API](../04-api/README.md). Un requisito sin correspondencia se considera no implementado.

```mermaid
flowchart LR
  REQ001[REQ-001 llega en menos de 10 s] --> PUSH["/notes/push"]
  REQ002[REQ-002 se envía al reconectar] --> QUEUE[Cola en el dispositivo]
  REQ003[REQ-003 detección de conflictos] --> VERSION[Cotejo del número de versión]
  REQ004[REQ-004 resolución automática] --> MERGE[Fusión a tres bandas]
  QUEUE --> PUSH
  VERSION --> MERGE
```
