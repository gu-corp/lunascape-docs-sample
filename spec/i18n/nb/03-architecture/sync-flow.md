---
navigation:
  order: 20
---

# 3.2 Synkroniseringsflyten

```mermaid
sequenceDiagram
  participant A as Enhet A
  participant S as Synkroniserings-API
  participant B as Enhet B
  A->>S: push(note, baseVersion=4)
  S->>S: tildel versjon 5
  S-->>A: 200 {version: 5}
  S-->>B: varsle(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Endringen fra enhet A får en ny versjon på serveren, og enhet B henter den når den har fått varselet. Varselet er et signal om å hente; det inneholder ikke selve teksten.
