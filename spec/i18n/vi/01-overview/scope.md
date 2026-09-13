---
navigation:
  order: 20
---

# 1.2 Phạm vi và giả định

## Phạm vi

| Mục | Thuộc phạm vi | Ngoài phạm vi |
|---|---|---|
| 1 | Đồng bộ việc tạo, cập nhật và xóa ghi chú | Đồng biên tập ghi chú (chia sẻ con trỏ khi cùng sửa) |
| 2 | Phát hiện và giải quyết xung đột giữa các thiết bị | Trình biên tập trên thiết bị |
| 3 | API đồng bộ (HTTP) | Thanh toán, quản lý tài khoản |

## Giả định

- Thiết bị chỉ kết nối không liên tục. Việc chỉnh sửa ngoại tuyến được xem là mặc định.
- Nội dung của một ghi chú tối đa là 1 MB.
- Thứ tự không phụ thuộc vào đồng hồ của thiết bị mà do số phiên bản của máy chủ quyết định.
