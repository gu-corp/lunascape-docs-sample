---
navigation:
  order: 20
---

# 3.2 Il flusso di sincronizzazione

```mermaid
sequenceDiagram
  participant A as Dispositivo A
  participant S as API di sincronizzazione
  participant B as Dispositivo B
  A->>S: push(note, baseVersion=4)
  S->>S: assegna la versione 5
  S-->>A: 200 {version: 5}
  S-->>B: notifica(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

La modifica del dispositivo A ottiene una nuova versione sul server e il dispositivo B, una volta ricevuta la notifica, la scarica. La notifica è un segnale che invita a scaricare: non trasporta il corpo del documento.
