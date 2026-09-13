---
navigation:
  order: 20
---

# 3.2 Przebieg synchronizacji

```mermaid
sequenceDiagram
  participant A as Urządzenie A
  participant S as API synchronizacji
  participant B as Urządzenie B
  A->>S: push(note, baseVersion=4)
  S->>S: nadanie wersji 5
  S-->>A: 200 {version: 5}
  S-->>B: powiadomienie(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Zmiana z urządzenia A otrzymuje na serwerze nową wersję, a urządzenie B pobiera ją po otrzymaniu powiadomienia. Powiadomienie jest sygnałem zachęcającym do pobrania — nie przenosi treści.
