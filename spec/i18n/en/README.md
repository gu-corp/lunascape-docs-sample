# Orbit Note Sync — Functional Specification

| Item | Value |
|---|---|
| Document ID | ORB-SPEC-001 |
| Version | 1.3 |
| Last updated | 2026-09-06 |
| Status | Approved |
| Document owner | Orbit team (fictional) |
| Related | ORB-REQ-001 (requirements), ORB-ADR-0001 (choice of sync method) |

## Revision history

| Version | Date | Description | Author |
|---|---|---|---|
| 1.0 | 2026-07-01 | Initial release | Orbit team |
| 1.1 | 2026-08-10 | Conflict resolution rules added (3.4) | Orbit team |
| 1.2 | 2026-09-06 | API error table added (4.3) | Orbit team |
| 1.3 | 2026-09-06 | Reorganized into one folder per chapter | Orbit team |

## Structure

1. [Overview](01-overview/README.md) — purpose, [scope and assumptions](01-overview/scope.md), [terms](01-overview/terms.md)
2. [Requirements](02-requirements/README.md) — [functional](02-requirements/functional.md), [non-functional](02-requirements/non-functional.md), [traceability](02-requirements/traceability.md)
3. [Architecture](03-architecture/README.md) — [components](03-architecture/components.md), [the sync flow](03-architecture/sync-flow.md), [versioning](03-architecture/versioning.md), [conflicts](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [endpoints](04-api/endpoints.md), [request and response](04-api/push.md), [errors](04-api/errors.md)
5. [Decisions](05-decisions/README.md) — [ORB-ADR-0001, the choice of sync method](05-decisions/0001-sync-method.md)

> **About this document**
> A fictional specification written as an example of what Lunascape Docs can carry. No such product or company exists. It shows one folder per chapter, tables, diagrams (Mermaid), code and translations in use. Pages without an English edition are shown in Japanese.
