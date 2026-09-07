---
navigation:
  order: 30
---

# 3.3 Version numbers

The version number is a monotonically increasing integer the server assigns per note. A device sends the last version it received as `baseVersion`. When the server's current version does not match `baseVersion`, that is a conflict (REQ-003). Device clocks play no part in ordering ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
