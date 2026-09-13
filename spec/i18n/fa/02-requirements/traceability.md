---
navigation:
  order: 30
---

# ۲.۳ ردیابی الزامات

هر الزام به عناصر [معماری](../03-architecture/README.md) و نقاط پایانی [API](../04-api/README.md) نگاشت می‌شود. الزامی که نگاشتی ندارد، پیاده‌سازی‌نشده در نظر گرفته می‌شود.

```mermaid
flowchart LR
  REQ001[REQ-001 دریافت ظرف ۱۰ ثانیه] --> PUSH["/notes/push"]
  REQ002[REQ-002 ارسال هنگام اتصال مجدد] --> QUEUE[صف سمت دستگاه]
  REQ003[REQ-003 تشخیص تعارض] --> VERSION[مقابلهٔ شمارهٔ نسخه]
  REQ004[REQ-004 حل خودکار] --> MERGE[ادغام سه‌طرفه]
  QUEUE --> PUSH
  VERSION --> MERGE
```
