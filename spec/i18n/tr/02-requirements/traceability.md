---
navigation:
  order: 30
---

# 2.3 Gereksinimlerin izlenmesi

Gereksinimler, [mimarinin](../03-architecture/README.md) her bir öğesiyle ve [API'nin](../04-api/README.md) her bir uç noktasıyla eşleştirilir. Eşleşmesi olmayan bir gereksinim, uygulanmamış sayılır.

```mermaid
flowchart LR
  REQ001[REQ-001 10 saniye içinde ulaşır] --> PUSH["/notes/push"]
  REQ002[REQ-002 yeniden bağlanınca gönderilir] --> QUEUE[Cihaz tarafındaki kuyruk]
  REQ003[REQ-003 çakışmanın saptanması] --> VERSION[Sürüm numarası denetimi]
  REQ004[REQ-004 otomatik çözüm] --> MERGE[Üç yönlü birleştirme]
  QUEUE --> PUSH
  VERSION --> MERGE
```
