---
navigation:
  order: 20
---

# 3.2 सिंक का प्रवाह

```mermaid
sequenceDiagram
  participant A as डिवाइस A
  participant S as सिंक API
  participant B as डिवाइस B
  A->>S: push(note, baseVersion=4)
  S->>S: संस्करण 5 निर्दिष्ट करें
  S-->>A: 200 {version: 5}
  S-->>B: सूचना(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

डिवाइस A का परिवर्तन सर्वर पर नया संस्करण पाता है, और सूचना मिलने पर डिवाइस B उसे प्राप्त करता है। सूचना प्राप्ति का संकेत भर है; वह मुख्य सामग्री नहीं ले जाती।
