---
navigation:
  order: 20
---

# 3.2 Поток синхронизации

```mermaid
sequenceDiagram
  participant A as Устройство A
  participant S as API синхронизации
  participant B as Устройство B
  A->>S: push(note, baseVersion=4)
  S->>S: присвоить версию 5
  S-->>A: 200 {version: 5}
  S-->>B: уведомление(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Изменение с устройства A получает на сервере новую версию, а устройство B, получив уведомление, забирает её. Уведомление — это сигнал к получению, оно не несёт самого текста.
