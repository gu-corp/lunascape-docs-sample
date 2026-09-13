---
navigation:
  order: 20
---

# 3.2 Synkronoinnin kulku

```mermaid
sequenceDiagram
  participant A as Laite A
  participant S as Synkronointi-API
  participant B as Laite B
  A->>S: push(note, baseVersion=4)
  S->>S: numeroi version 5:ksi
  S-->>A: 200 {version: 5}
  S-->>B: ilmoitus(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Laitteen A muutos saa palvelimella uuden version, ja ilmoituksen saanut laite B noutaa sen. Ilmoitus on kehotus noutaa; se ei kuljeta sisältöä.
