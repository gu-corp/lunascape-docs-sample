---
navigation:
  order: 30
---

# 4.3 Lỗi

| Trạng thái | Ý nghĩa | Cách xử lý của thiết bị |
|---|---|---|
| 400 | Yêu cầu sai định dạng | Ngừng gửi và ghi vào nhật ký |
| 401 | Token không hợp lệ | Xác thực lại |
| 409 | Phiên bản không khớp (xung đột) | Thay thế bằng `body` của phản hồi và hiển thị là có xung đột |
| 413 | Phần thân vượt quá 1 MB | Báo cho người dùng và không gửi |
| 429 | Quá nhiều yêu cầu | Chờ đúng số giây nêu trong `Retry-After` rồi gửi lại |
| 5xx | Sự cố máy chủ | Gửi lại theo lối lùi thời gian theo cấp số nhân (tối đa 5 lần) |
