---
navigation:
  order: 20
---

# 3.2 Le flux de synchronisation

```mermaid
sequenceDiagram
  participant A as Appareil A
  participant S as API de synchronisation
  participant B as Appareil B
  A->>S: push(note, baseVersion=4)
  S->>S: attribue la version 5
  S-->>A: 200 {version: 5}
  S-->>B: notification(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

La modification de l'appareil A obtient une nouvelle version sur le serveur, et l'appareil B la récupère une fois notifié. La notification est un signal qui invite à récupérer ; elle ne transporte pas le corps du document.
