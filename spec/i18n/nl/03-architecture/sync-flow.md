---
navigation:
  order: 20
---

# 3.2 Het synchronisatieverloop

```mermaid
sequenceDiagram
  participant A as Apparaat A
  participant S as Sync-API
  participant B as Apparaat B
  A->>S: push(note, baseVersion=4)
  S->>S: versie 5 toekennen
  S-->>A: 200 {version: 5}
  S-->>B: melding(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

De wijziging van apparaat A krijgt op de server een nieuwe versie, en apparaat B haalt die op zodra het een melding heeft gekregen. De melding is een signaal om op te halen; ze bevat de inhoud niet.
