---
navigation:
  order: 30
---

# 3.3 Số phiên bản

Số phiên bản là một số nguyên tăng đơn điệu do máy chủ cấp cho từng ghi chú. Thiết bị gửi phiên bản cuối cùng mà nó nhận được dưới dạng `baseVersion`. Khi phiên bản hiện tại của máy chủ không khớp với `baseVersion`, đó là một xung đột (REQ-003). Đồng hồ của thiết bị không được dùng để xác định thứ tự ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
