---
navigation:
  order: 10
---

# 1. Overview

## 1.1 Purpose

Orbit synchronizes plain-text notes edited on several devices without any action by the user. This document defines its functions, external interfaces and constraints.

## 1.2 Scope

| No. | In scope | Out of scope |
|---|---|---|
| 1 | Syncing note creation, updates and deletion | Collaborative editing (shared cursors) |
| 2 | Detecting and resolving conflicts between devices | The editor on the device |
| 3 | The sync API (HTTP) | Billing, account management |

## 1.3 Terms

| Term | Definition |
|---|---|
| Note | One text file, with an id, a body, an update time and a version number |
| Device | A machine running the Orbit client, identified by a device id |
| Version | An integer that grows by one per update; the server assigns it |
| Conflict | Two devices updated the same version of a note independently |
| Convergence | Every device holds the same content for a note |

## 1.4 Assumptions

- Devices connect intermittently; editing offline is the normal case.
- A note's body is at most 1 MB.
- Ordering never depends on device clocks; the server's version numbers decide.
