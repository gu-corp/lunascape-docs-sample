---
navigation:
  order: 10
---

# 2.1 Yêu cầu chức năng

| ID | Yêu cầu | Mức ưu tiên | Phương pháp kiểm chứng |
|---|---|---|---|
| REQ-001 | Ghi chú được tạo trên một thiết bị sẽ đến các thiết bị khác trong vòng 10 giây sau khi kết nối | Bắt buộc | Kiểm thử tích hợp |
| REQ-002 | Ghi chú được chỉnh sửa khi ngoại tuyến sẽ tự động được gửi đi khi kết nối lại | Bắt buộc | Kiểm thử tích hợp |
| REQ-003 | Hai bản cập nhật trên cùng một phiên bản được phát hiện là xung đột | Bắt buộc | Kiểm thử đơn vị |
| REQ-004 | Xung đột được giải quyết tự động theo [quy tắc ở mục 3.4](../03-architecture/conflicts.md), không làm mất nội dung của cả hai bên | Bắt buộc | Kiểm thử đơn vị |
| REQ-005 | Việc xóa được phản ánh sang các thiết bị khác và có thể khôi phục từ Thùng rác trong 30 ngày | Khuyến nghị | Kiểm thử tích hợp |
| REQ-006 | Thiết bị có thể hiển thị trạng thái đồng bộ (đã đồng bộ, đang gửi, có xung đột) | Khuyến nghị | Kiểm tra trực quan |
