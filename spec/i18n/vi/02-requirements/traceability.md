---
navigation:
  order: 30
---

# 2.3 Truy vết yêu cầu

Mỗi yêu cầu được ánh xạ tới các thành phần trong [kiến trúc](../03-architecture/README.md) và các điểm cuối của [API](../04-api/README.md). Yêu cầu không có ánh xạ được xem là chưa hiện thực.

```mermaid
flowchart LR
  REQ001[REQ-001 đến nơi trong vòng 10 giây] --> PUSH["/notes/push"]
  REQ002[REQ-002 gửi khi kết nối lại] --> QUEUE[Hàng đợi phía thiết bị]
  REQ003[REQ-003 phát hiện xung đột] --> VERSION[Đối chiếu số phiên bản]
  REQ004[REQ-004 tự động giải quyết] --> MERGE[Hợp nhất 3 chiều]
  QUEUE --> PUSH
  VERSION --> MERGE
```
