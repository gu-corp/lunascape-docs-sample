---
navigation:
  order: 20
---

# 3.2 Η ροή συγχρονισμού

```mermaid
sequenceDiagram
  participant A as Συσκευή A
  participant S as API συγχρονισμού
  participant B as Συσκευή B
  A->>S: push(note, baseVersion=4)
  S->>S: εκχώρηση έκδοσης 5
  S-->>A: 200 {version: 5}
  S-->>B: ειδοποίηση(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Η αλλαγή της συσκευής A λαμβάνει νέα έκδοση στον διακομιστή και η συσκευή B, αφού ειδοποιηθεί, την ανακτά. Η ειδοποίηση είναι σήμα που προτρέπει την ανάκτηση· δεν μεταφέρει το σώμα του κειμένου.
