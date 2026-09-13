---
navigation:
  order: 20
---

# 3.2 Fluxul de sincronizare

```mermaid
sequenceDiagram
  participant A as Dispozitivul A
  participant S as API de sincronizare
  participant B as Dispozitivul B
  A->>S: push(note, baseVersion=4)
  S->>S: atribuie versiunea 5
  S-->>A: 200 {version: 5}
  S-->>B: notificare(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Modificarea de pe dispozitivul A primește o versiune nouă pe server, iar dispozitivul B o preia după ce este notificat. Notificarea este doar un semnal care îndeamnă la preluare; ea nu transportă conținutul.
