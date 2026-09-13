---
navigation:
  order: 30
---

# 2.3 Traçabilité des exigences

Les exigences sont mises en correspondance avec les éléments de [l'architecture](../03-architecture/README.md) et les points de terminaison de [l'API](../04-api/README.md). Une exigence sans correspondance est considérée comme non implémentée.

```mermaid
flowchart LR
  REQ001[REQ-001 arrive en moins de 10 s] --> PUSH["/notes/push"]
  REQ002[REQ-002 envoi à la reconnexion] --> QUEUE[File d'attente côté appareil]
  REQ003[REQ-003 détection des conflits] --> VERSION[Vérification du numéro de version]
  REQ004[REQ-004 résolution automatique] --> MERGE[Fusion à trois voies]
  QUEUE --> PUSH
  VERSION --> MERGE
```
