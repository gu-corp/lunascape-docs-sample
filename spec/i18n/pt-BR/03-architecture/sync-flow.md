---
navigation:
  order: 20
---

# 3.2 O fluxo de sincronização

```mermaid
sequenceDiagram
  participant A as Dispositivo A
  participant S as API de sincronização
  participant B as Dispositivo B
  A->>S: push(note, baseVersion=4)
  S->>S: atribui a versão 5
  S-->>A: 200 {version: 5}
  S-->>B: notificação(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

A alteração do dispositivo A recebe uma nova versão no servidor, e o dispositivo B a obtém depois de ser notificado. A notificação é apenas um aviso para obter o conteúdo; ela não transporta o corpo do documento.
