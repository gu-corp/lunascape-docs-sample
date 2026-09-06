# Orbit ノート同期サービス 機能仕様書

| 項目 | 内容 |
|---|---|
| 文書ID | ORB-SPEC-001 |
| 版 | 1.3 |
| 更新日 | 2026-09-06 |
| 状態 | 承認済み |
| 文書責任者 | Orbit 開発チーム（架空） |
| 関連 | ORB-REQ-001（要件一覧）、ORB-ADR-0001（同期方式の選定） |

## 改訂履歴

| 版 | 日付 | 改訂内容 | 改訂者 |
|---|---|---|---|
| 1.0 | 2026-07-01 | 初版 | Orbit 開発チーム |
| 1.1 | 2026-08-10 | 競合解決の規則を追加（3.4） | Orbit 開発チーム |
| 1.2 | 2026-09-06 | API のエラー表を追加（4.3） | Orbit 開発チーム |
| 1.3 | 2026-09-06 | 章ごとのフォルダー構成に改める | Orbit 開発チーム |

## 構成

1. [概要](01-overview/README.md) — 目的、[範囲と前提](01-overview/scope.md)、[用語](01-overview/terms.md)
2. [要件](02-requirements/README.md) — [機能要件](02-requirements/functional.md)、[非機能要件](02-requirements/non-functional.md)、[要件の追跡](02-requirements/traceability.md)
3. [構成](03-architecture/README.md) — [構成要素](03-architecture/components.md)、[同期の流れ](03-architecture/sync-flow.md)、[版番号](03-architecture/versioning.md)、[競合の解決](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [エンドポイント](04-api/endpoints.md)、[要求と応答](04-api/push.md)、[エラー](04-api/errors.md)
5. [設計判断](05-decisions/README.md) — [ORB-ADR-0001 同期方式の選定](05-decisions/0001-sync-method.md)

> **この文書について**
> Lunascape Docs の書き方の例として作った架空の仕様書です。製品や会社は実在しません。章ごとのフォルダー、表、図（Mermaid）、コード、翻訳の使い方を見るためのものです。
