---
navigation:
  order: 30
---

# 2.3 تتبّع المتطلبات

تُربَط المتطلبات بعناصر [البنية](../03-architecture/README.md) وبنقاط نهاية [واجهة البرمجة](../04-api/README.md). ويُعدّ أي متطلب بلا ارتباط غير منفَّذ.

```mermaid
flowchart LR
  REQ001[REQ-001 يصل خلال 10 ثوانٍ] --> PUSH["/notes/push"]
  REQ002[REQ-002 يُرسَل عند إعادة الاتصال] --> QUEUE[طابور على الجهاز]
  REQ003[REQ-003 كشف التعارض] --> VERSION[مطابقة رقم الإصدار]
  REQ004[REQ-004 حلّ تلقائي] --> MERGE[دمج ثلاثي الاتجاه]
  QUEUE --> PUSH
  VERSION --> MERGE
```
