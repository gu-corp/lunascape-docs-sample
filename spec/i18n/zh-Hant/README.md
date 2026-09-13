# Orbit 筆記同步服務 功能規格書

| 項目 | 內容 |
|---|---|
| 文件 ID | ORB-SPEC-001 |
| 版本 | 1.3 |
| 更新日期 | 2026-09-06 |
| 狀態 | 已核准 |
| 文件負責人 | Orbit 開發團隊（虛構） |
| 相關文件 | ORB-REQ-001（需求一覽）、ORB-ADR-0001（同步方式的選定） |

## 修訂記錄

| 版本 | 日期 | 修訂內容 | 修訂者 |
|---|---|---|---|
| 1.0 | 2026-07-01 | 初版 | Orbit 開發團隊 |
| 1.1 | 2026-08-10 | 新增衝突解決規則（3.4） | Orbit 開發團隊 |
| 1.2 | 2026-09-06 | 新增 API 錯誤表（4.3） | Orbit 開發團隊 |
| 1.3 | 2026-09-06 | 改為每章一個資料夾的結構 | Orbit 開發團隊 |

## 架構

1. [概觀](01-overview/README.md) — 目的、[範圍與前提](01-overview/scope.md)、[術語](01-overview/terms.md)
2. [需求](02-requirements/README.md) — [功能需求](02-requirements/functional.md)、[非功能需求](02-requirements/non-functional.md)、[需求追蹤](02-requirements/traceability.md)
3. [架構](03-architecture/README.md) — [組成元件](03-architecture/components.md)、[同步流程](03-architecture/sync-flow.md)、[版本編號](03-architecture/versioning.md)、[衝突的解決](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [端點](04-api/endpoints.md)、[要求與回應](04-api/push.md)、[錯誤](04-api/errors.md)
5. [設計判斷](05-decisions/README.md) — [ORB-ADR-0001 同步方式的選定](05-decisions/0001-sync-method.md)

> **關於本文件**
> 這是為了示範 Lunascape Docs 的撰寫方式而製作的虛構規格書。文中的產品與公司並不存在。用途是呈現每章一個資料夾、表格、圖表（Mermaid）、程式碼與翻譯的使用方式。
