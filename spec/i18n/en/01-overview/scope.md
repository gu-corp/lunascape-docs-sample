---
navigation:
  order: 20
---

# 1.2 Scope and assumptions

## Scope

| No. | In scope | Out of scope |
|---|---|---|
| 1 | Syncing note creation, updates and deletion | Collaborative editing (shared cursors) |
| 2 | Detecting and resolving conflicts between devices | The editor on the device |
| 3 | The sync API (HTTP) | Billing, account management |

## Assumptions

- Devices connect intermittently; editing offline is the normal case.
- A note's body is at most 1 MB.
- Ordering never depends on device clocks; the server's version numbers decide.
