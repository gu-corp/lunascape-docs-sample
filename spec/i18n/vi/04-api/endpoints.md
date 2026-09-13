---
navigation:
  order: 10
---

# 4.1 Điểm cuối

| Phương thức | Đường dẫn | Mục đích | Yêu cầu |
|---|---|---|---|
| POST | `/notes/push` | Gửi thay đổi của ghi chú | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Nhận các thay đổi sau phiên bản đã chỉ định | REQ-001 |
| DELETE | `/notes/{id}` | Xóa ghi chú (chuyển vào Thùng rác) | REQ-005 |
| POST | `/notes/{id}/restore` | Khôi phục từ Thùng rác | REQ-005 |
