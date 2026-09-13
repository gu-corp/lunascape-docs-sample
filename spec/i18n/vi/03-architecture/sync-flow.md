---
navigation:
  order: 20
---

# 3.2 Luồng đồng bộ

```mermaid
sequenceDiagram
  participant A as Thiết bị A
  participant S as API đồng bộ
  participant B as Thiết bị B
  A->>S: push(note, baseVersion=4)
  S->>S: gán phiên bản 5
  S-->>A: 200 {version: 5}
  S-->>B: thông báo(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Thay đổi ở thiết bị A nhận một phiên bản mới trên máy chủ, và thiết bị B lấy về sau khi nhận thông báo. Thông báo chỉ là tín hiệu nhắc lấy về; nó không mang theo nội dung.
