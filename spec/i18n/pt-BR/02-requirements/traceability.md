---
navigation:
  order: 30
---

# 2.3 Rastreabilidade dos requisitos

Os requisitos são associados a cada elemento da [arquitetura](../03-architecture/README.md) e a cada endpoint da [API](../04-api/README.md). Um requisito sem associação é tratado como não implementado.

```mermaid
flowchart LR
  REQ001[REQ-001 chega em até 10 s] --> PUSH["/notes/push"]
  REQ002[REQ-002 envio na reconexão] --> QUEUE[Fila no dispositivo]
  REQ003[REQ-003 detecção de conflitos] --> VERSION[Conferência do número de versão]
  REQ004[REQ-004 resolução automática] --> MERGE[Mesclagem de três vias]
  QUEUE --> PUSH
  VERSION --> MERGE
```
