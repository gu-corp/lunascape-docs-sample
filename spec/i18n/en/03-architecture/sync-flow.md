---
navigation:
  order: 20
---

# 3.2 The sync flow

```mermaid
sequenceDiagram
  participant A as Device A
  participant S as Sync API
  participant B as Device B
  A->>S: push(note, baseVersion=4)
  S->>S: assign version 5
  S-->>A: 200 {version: 5}
  S-->>B: notify(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Device A's change gets a new version on the server, and device B pulls it once notified. The notification is a prompt to pull; it carries no body.
