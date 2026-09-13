---
navigation:
  order: 20
---

# ۳.۲ جریان همگام‌سازی

```mermaid
sequenceDiagram
  participant A as دستگاه A
  participant S as API همگام‌سازی
  participant B as دستگاه B
  A->>S: push(note, baseVersion=4)
  S->>S: تخصیص نسخهٔ ۵
  S-->>A: 200 {version: 5}
  S-->>B: اعلان(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

تغییر دستگاه A روی سرور نسخهٔ تازه‌ای می‌گیرد و دستگاه B پس از دریافت اعلان آن را می‌گیرد. اعلان تنها نشانه‌ای برای دریافت است و متن را با خود نمی‌آورد.
