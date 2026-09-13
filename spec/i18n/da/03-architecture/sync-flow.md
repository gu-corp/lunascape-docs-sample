---
navigation:
  order: 20
---

# 3.2 Synkroniseringsforløbet

```mermaid
sequenceDiagram
  participant A as Enhed A
  participant S as Synkroniserings-API
  participant B as Enhed B
  A->>S: push(note, baseVersion=4)
  S->>S: tildel version 5
  S-->>A: 200 {version: 5}
  S-->>B: notifikation(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Ændringen fra enhed A får en ny version på serveren, og enhed B henter den, når den har fået besked. Notifikationen er blot et signal om at hente; den indeholder ikke selve indholdet.
