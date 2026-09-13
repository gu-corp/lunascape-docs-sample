---
navigation:
  order: 40
---

# 3.4 Giải quyết xung đột

| Trường hợp | Quy tắc |
|---|---|
| Cùng một dòng bị thay đổi riêng rẽ ở hai bên | Giữ lại cả hai thay đổi: thay đổi đến sau được thêm vào cuối, ngăn cách bằng `>>>`. Hiển thị cho người dùng là có xung đột (REQ-006) |
| Các dòng khác nhau bị thay đổi | Tự động hợp nhất bằng phép hợp nhất ba chiều; không thông báo cho người dùng |
| Một bên đã xóa | Ưu tiên việc xóa, nội dung của bên còn lại được đưa vào Thùng rác (REQ-005) |

Trong mọi trường hợp, không có nội dung nào bị mất (REQ-004).
