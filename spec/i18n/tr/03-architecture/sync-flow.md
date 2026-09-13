---
navigation:
  order: 20
---

# 3.2 Eşitleme akışı

```mermaid
sequenceDiagram
  participant A as Aygıt A
  participant S as Eşitleme API'si
  participant B as Aygıt B
  A->>S: push(note, baseVersion=4)
  S->>S: sürümü 5 olarak numaralandır
  S-->>A: 200 {version: 5}
  S-->>B: bildir(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Aygıt A'daki değişiklik sunucuda yeni bir sürüm alır; bildirimi alan aygıt B de bunu çeker. Bildirim, çekmeyi isteyen bir işarettir; gövdeyi taşımaz.
