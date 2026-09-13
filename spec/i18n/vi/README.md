# Dịch vụ đồng bộ ghi chú Orbit — Bản đặc tả chức năng

| Mục | Nội dung |
|---|---|
| Mã tài liệu | ORB-SPEC-001 |
| Phiên bản | 1.3 |
| Ngày cập nhật | 2026-09-06 |
| Trạng thái | Đã phê duyệt |
| Người phụ trách tài liệu | Nhóm phát triển Orbit (hư cấu) |
| Liên quan | ORB-REQ-001 (danh sách yêu cầu), ORB-ADR-0001 (lựa chọn phương thức đồng bộ) |

## Lịch sử sửa đổi

| Phiên bản | Ngày | Nội dung sửa đổi | Người sửa đổi |
|---|---|---|---|
| 1.0 | 2026-07-01 | Bản đầu tiên | Nhóm phát triển Orbit |
| 1.1 | 2026-08-10 | Bổ sung quy tắc giải quyết xung đột (3.4) | Nhóm phát triển Orbit |
| 1.2 | 2026-09-06 | Bổ sung bảng lỗi của API (4.3) | Nhóm phát triển Orbit |
| 1.3 | 2026-09-06 | Sắp xếp lại thành một thư mục cho mỗi chương | Nhóm phát triển Orbit |

## Cấu trúc

1. [Tổng quan](01-overview/README.md) — mục đích, [phạm vi và giả định](01-overview/scope.md), [thuật ngữ](01-overview/terms.md)
2. [Yêu cầu](02-requirements/README.md) — [yêu cầu chức năng](02-requirements/functional.md), [yêu cầu phi chức năng](02-requirements/non-functional.md), [truy vết yêu cầu](02-requirements/traceability.md)
3. [Kiến trúc](03-architecture/README.md) — [thành phần cấu tạo](03-architecture/components.md), [luồng đồng bộ](03-architecture/sync-flow.md), [số phiên bản](03-architecture/versioning.md), [giải quyết xung đột](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [điểm cuối](04-api/endpoints.md), [yêu cầu và phản hồi](04-api/push.md), [lỗi](04-api/errors.md)
5. [Quyết định thiết kế](05-decisions/README.md) — [ORB-ADR-0001 Lựa chọn phương thức đồng bộ](05-decisions/0001-sync-method.md)

> **Về tài liệu này**
> Đây là một bản đặc tả hư cấu, được viết làm ví dụ về cách viết trong Lunascape Docs. Sản phẩm và công ty nêu ở đây không có thật. Tài liệu này nhằm cho thấy cách dùng thư mục theo từng chương, bảng, sơ đồ (Mermaid), mã nguồn và bản dịch.
