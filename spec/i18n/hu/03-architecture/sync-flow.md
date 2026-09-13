---
navigation:
  order: 20
---

# 3.2 A szinkronizálás folyamata

```mermaid
sequenceDiagram
  participant A as A eszköz
  participant S as Szinkronizációs API
  participant B as B eszköz
  A->>S: push(note, baseVersion=4)
  S->>S: verzió kiosztása: 5
  S-->>A: 200 {version: 5}
  S-->>B: értesítés(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Az A eszköz módosítása a szerveren új verziót kap, és az értesítést megkapó B eszköz letölti azt. Az értesítés csak jelzés a letöltésre, a törzsszöveget nem szállítja.
