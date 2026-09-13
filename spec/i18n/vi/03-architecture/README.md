---
navigation:
  order: 30
---

# 3. Kiến trúc

Đồng bộ được tạo thành từ bốn yếu tố: máy khách, API đồng bộ, kho lưu trữ dữ liệu và thông báo ([thành phần cấu tạo](components.md)). [Luồng đồng bộ](sync-flow.md) trình bày thứ tự mà một thay đổi đi từ thiết bị đến máy chủ, rồi từ máy chủ đến các thiết bị khác. Cơ sở của thứ tự đó là [số phiên bản](versioning.md); cách xử lý khi hai bản cập nhật cùng rơi vào một phiên bản được quy định trong [giải quyết xung đột](conflicts.md).
