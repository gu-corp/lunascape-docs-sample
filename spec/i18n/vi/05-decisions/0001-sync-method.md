---
navigation:
  order: 10
---

# ORB-ADR-0001: Chọn "phiên bản do máy chủ đánh số và hợp nhất ba chiều" làm phương thức đồng bộ

| Mục | Nội dung |
|---|---|
| Mã tài liệu | ORB-ADR-0001 |
| Phiên bản | 1.0 |
| Ngày cập nhật | 2026-07-01 |
| Trạng thái | Đã phê duyệt |

## 1. Bối cảnh

Ghi chú được chỉnh sửa ngoại tuyến trên nhiều thiết bị cần hội tụ về một bản. Có ba phương án: (a) bản ghi sau cùng thắng theo thời điểm cập nhật, (b) CRDT, (c) số phiên bản do máy chủ đánh số kèm hợp nhất ba chiều.

## 2. Quyết định

| Số | Nội dung quyết định |
|---|---|
| 1 | Thứ tự được quyết định bằng số phiên bản do máy chủ đánh số. Không tin vào đồng hồ của thiết bị |
| 2 | Xung đột được giải quyết bằng hợp nhất ba chiều; dòng nào không giải quyết được thì giữ lại cả hai bên. Ưu tiên không làm mất nội dung |
| 3 | Không dùng CRDT. Ghi chú vốn ngắn, không có nhu cầu chỉnh sửa đồng thời, và việc kích thước nội dung tăng gấp đôi trở lên là cái giá không tương xứng |

## 3. Ảnh hưởng

| Số | Ảnh hưởng |
|---|---|
| 1 | Thiết bị giữ `baseVersion` và đính kèm mỗi lần gửi |
| 2 | Việc hiển thị xung đột (REQ-006) trở thành tính năng bắt buộc của thiết bị |
| 3 | Máy chủ giữ lịch sử 30 ngày gần nhất (dùng cho Thùng rác và làm cơ sở cho hợp nhất ba chiều) |
