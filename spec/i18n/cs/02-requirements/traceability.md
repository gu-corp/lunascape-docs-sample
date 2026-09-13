---
navigation:
  order: 30
---

# 2.3 Sledovatelnost požadavků

Požadavky se přiřazují k jednotlivým prvkům [architektury](../03-architecture/README.md) a k jednotlivým koncovým bodům [API](../04-api/README.md). Požadavek bez přiřazení se považuje za neimplementovaný.

```mermaid
flowchart LR
  REQ001[REQ-001 doručení do 10 s] --> PUSH["/notes/push"]
  REQ002[REQ-002 odeslání při obnovení spojení] --> QUEUE[Fronta na straně zařízení]
  REQ003[REQ-003 detekce konfliktů] --> VERSION[Porovnání čísla verze]
  REQ004[REQ-004 automatické řešení] --> MERGE[Třícestné sloučení]
  QUEUE --> PUSH
  VERSION --> MERGE
```
