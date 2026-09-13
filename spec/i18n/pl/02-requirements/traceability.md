---
navigation:
  order: 30
---

# 2.3 Śledzenie wymagań

Wymagania są przyporządkowane do poszczególnych elementów [architektury](../03-architecture/README.md) oraz do poszczególnych punktów końcowych [API](../04-api/README.md). Wymaganie bez przyporządkowania traktuje się jako niezaimplementowane.

```mermaid
flowchart LR
  REQ001[REQ-001 dociera w ciągu 10 s] --> PUSH["/notes/push"]
  REQ002[REQ-002 wysyłka po ponownym połączeniu] --> QUEUE[Kolejka po stronie urządzenia]
  REQ003[REQ-003 wykrywanie konfliktów] --> VERSION[Porównanie numerów wersji]
  REQ004[REQ-004 automatyczne rozwiązywanie] --> MERGE[Scalanie trójstronne]
  QUEUE --> PUSH
  VERSION --> MERGE
```
