---
navigation:
  order: 20
---

# 3.2 Synkroniseringsflödet

```mermaid
sequenceDiagram
  participant A as Enhet A
  participant S as Synk-API
  participant B as Enhet B
  A->>S: push(note, baseVersion=4)
  S->>S: tilldela version 5
  S-->>A: 200 {version: 5}
  S-->>B: avisera(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Ändringen på enhet A får en ny version på servern, och enhet B hämtar den när den har aviserats. Aviseringen är en signal om att hämta; den bär inte med sig något innehåll.
