---
navigation:
  order: 20
---

# 3.2 Tijek sinkronizacije

```mermaid
sequenceDiagram
  participant A as Uređaj A
  participant S as API za sinkronizaciju
  participant B as Uređaj B
  A->>S: push(note, baseVersion=4)
  S->>S: dodjela verzije 5
  S-->>A: 200 {version: 5}
  S-->>B: obavijest(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Promjena s uređaja A dobiva novu verziju na poslužitelju, a uređaj B je preuzima nakon što primi obavijest. Obavijest je poticaj na preuzimanje; ona ne prenosi sadržaj.
