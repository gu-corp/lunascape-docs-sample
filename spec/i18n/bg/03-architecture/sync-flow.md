---
navigation:
  order: 20
---

# 3.2 Протичане на синхронизацията

```mermaid
sequenceDiagram
  participant A as Устройство A
  participant S as API за синхронизация
  participant B as Устройство B
  A->>S: push(note, baseVersion=4)
  S->>S: присвоява версия 5
  S-->>A: 200 {version: 5}
  S-->>B: известие(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Промяната на устройство A получава нова версия на сървъра, а устройство B я изтегля, след като бъде известено. Известието е подкана за изтегляне; то не носи съдържанието.
