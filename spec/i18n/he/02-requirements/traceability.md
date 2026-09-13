---
navigation:
  order: 30
---

# 2.3 מעקב אחר דרישות

הדרישות ממופות לרכיבי [המבנה](../03-architecture/README.md) ולנקודות הקצה של [ה‑API](../04-api/README.md). דרישה ללא מיפוי נחשבת לבלתי ממומשת.

```mermaid
flowchart LR
  REQ001[REQ-001 מגיע תוך 10 שניות] --> PUSH["/notes/push"]
  REQ002[REQ-002 נשלח בעת חיבור מחדש] --> QUEUE[תור בצד המכשיר]
  REQ003[REQ-003 זיהוי התנגשות] --> VERSION[השוואת מספר גרסה]
  REQ004[REQ-004 פתרון אוטומטי] --> MERGE[מיזוג תלת‑כיווני]
  QUEUE --> PUSH
  VERSION --> MERGE
```
