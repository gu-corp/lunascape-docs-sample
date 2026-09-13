---
navigation:
  order: 20
---

# 3.2 ลำดับการซิงค์

```mermaid
sequenceDiagram
  participant A as อุปกรณ์ A
  participant S as API ซิงค์
  participant B as อุปกรณ์ B
  A->>S: push(note, baseVersion=4)
  S->>S: กำหนดเวอร์ชันเป็น 5
  S-->>A: 200 {version: 5}
  S-->>B: แจ้งเตือน(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

การเปลี่ยนแปลงของอุปกรณ์ A จะได้รับเวอร์ชันใหม่ที่เซิร์ฟเวอร์ แล้วอุปกรณ์ B ที่ได้รับการแจ้งเตือนจะดึงข้อมูลนั้นมา การแจ้งเตือนเป็นเพียงสัญญาณให้ดึงข้อมูล ไม่ได้นำเนื้อหามาด้วย
