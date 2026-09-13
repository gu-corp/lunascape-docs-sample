---
navigation:
  order: 20
---

# 3.2 El flujo de sincronización

```mermaid
sequenceDiagram
  participant A as Dispositivo A
  participant S as API de sincronización
  participant B as Dispositivo B
  A->>S: push(note, baseVersion=4)
  S->>S: asigna la versión 5
  S-->>A: 200 {version: 5}
  S-->>B: notifica(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

El cambio del dispositivo A obtiene una versión nueva en el servidor, y el dispositivo B, tras recibir la notificación, lo descarga. La notificación es una señal que invita a descargar; no transporta el cuerpo del texto.
