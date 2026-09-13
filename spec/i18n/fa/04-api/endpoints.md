---
navigation:
  order: 10
---

# ۴.۱ نقاط پایانی

| متد | مسیر | هدف | الزام |
|---|---|---|---|
| POST | `/notes/push` | ارسال تغییرات یک یادداشت | REQ-001، REQ-002 |
| GET | `/notes/pull?since=<version>` | دریافت تغییرات پس از نسخهٔ مشخص‌شده | REQ-001 |
| DELETE | `/notes/{id}` | حذف یادداشت (انتقال به سطل زباله) | REQ-005 |
| POST | `/notes/{id}/restore` | بازگرداندن از سطل زباله | REQ-005 |
