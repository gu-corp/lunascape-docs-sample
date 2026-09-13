---
navigation:
  order: 20
---

# 3.2 Процес синхронізації

```mermaid
sequenceDiagram
  participant A as Пристрій A
  participant S as API синхронізації
  participant B as Пристрій B
  A->>S: push(note, baseVersion=4)
  S->>S: призначає версію 5
  S-->>A: 200 {version: 5}
  S-->>B: сповіщення(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Зміна на пристрої A отримує на сервері нову версію, а пристрій B, отримавши сповіщення, завантажує її. Сповіщення — це лише сигнал завантажити зміну, воно не переносить сам текст.
