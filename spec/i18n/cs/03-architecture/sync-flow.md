---
navigation:
  order: 20
---

# 3.2 Průběh synchronizace

```mermaid
sequenceDiagram
  participant A as Zařízení A
  participant S as Synchronizační API
  participant B as Zařízení B
  A->>S: push(note, baseVersion=4)
  S->>S: přidělení verze 5
  S-->>A: 200 {version: 5}
  S-->>B: oznámení(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Změna ze zařízení A dostane na serveru novou verzi a zařízení B si ji po oznámení stáhne. Oznámení je pouze pokynem ke stažení, samotný obsah nepřenáší.
