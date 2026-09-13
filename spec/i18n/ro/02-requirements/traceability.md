---
navigation:
  order: 30
---

# 2.3 Trasabilitatea cerințelor

Cerințele se pun în corespondență cu elementele din [arhitectură](../03-architecture/README.md) și cu punctele finale din [API](../04-api/README.md). O cerință fără corespondență este considerată neimplementată.

```mermaid
flowchart LR
  REQ001[REQ-001 ajunge în 10 secunde] --> PUSH["/notes/push"]
  REQ002[REQ-002 trimis la reconectare] --> QUEUE[Coadă pe dispozitiv]
  REQ003[REQ-003 detectarea conflictelor] --> VERSION[Verificarea numărului de versiune]
  REQ004[REQ-004 rezolvare automată] --> MERGE[Îmbinare în trei direcții]
  QUEUE --> PUSH
  VERSION --> MERGE
```
