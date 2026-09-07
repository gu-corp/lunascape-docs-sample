---
navigation:
  order: 40
---

# 3.4 Conflict resolution

| Case | Rule |
|---|---|
| The same line was changed independently | Both changes are kept: the one that arrived later is appended, set off by `>>>`. The device shows a conflict (REQ-006) |
| Different lines were changed | Merged automatically by a three-way merge; the user is not told |
| One side deleted the note | The deletion wins, and the other side's content goes to the trash (REQ-005) |

In every case, no content is lost (REQ-004).
