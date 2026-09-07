---
navigation:
  order: 10
---

# ORB-ADR-0001: Choose "server-assigned versions with three-way merge" as the sync method

| Item | Value |
|---|---|
| Document ID | ORB-ADR-0001 |
| Version | 1.0 |
| Last updated | 2026-07-01 |
| Status | Approved |

## 1. Background

Notes edited offline on several devices need to converge. Three candidates were considered: (a) last-write-wins by timestamp, (b) a CRDT, (c) server-assigned version numbers with a three-way merge.

## 2. Decision

| No. | Decision |
|---|---|
| 1 | Order is decided by version numbers the server assigns; device clocks are not trusted |
| 2 | Conflicts are resolved by a three-way merge; a line that cannot be merged keeps both sides. Not losing content takes priority |
| 3 | A CRDT was not adopted: notes are short, there is no requirement for simultaneous editing, and doubling the body's size or more is not worth the cost |

## 3. Consequences

| No. | Consequence |
|---|---|
| 1 | A device holds `baseVersion` and attaches it to every send |
| 2 | Showing a conflict (REQ-006) becomes a required device feature |
| 3 | The server keeps 30 days of history (for the trash, and as the base for three-way merges) |
