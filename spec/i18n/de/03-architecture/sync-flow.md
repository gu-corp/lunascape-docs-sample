---
navigation:
  order: 20
---

# 3.2 Der Ablauf der Synchronisierung

```mermaid
sequenceDiagram
  participant A as Gerät A
  participant S as Sync-API
  participant B as Gerät B
  A->>S: push(note, baseVersion=4)
  S->>S: Version 5 vergeben
  S-->>A: 200 {version: 5}
  S-->>B: Benachrichtigung(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Die Änderung von Gerät A erhält auf dem Server eine neue Version, und Gerät B ruft sie nach der Benachrichtigung ab. Die Benachrichtigung ist ein Signal zum Abrufen; sie transportiert keinen Inhalt.
