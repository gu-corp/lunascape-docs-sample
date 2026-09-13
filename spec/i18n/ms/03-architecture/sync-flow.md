---
navigation:
  order: 20
---

# 3.2 Aliran penyegerakan

```mermaid
sequenceDiagram
  participant A as Peranti A
  participant S as API penyegerakan
  participant B as Peranti B
  A->>S: push(note, baseVersion=4)
  S->>S: umpuk versi 5
  S-->>A: 200 {version: 5}
  S-->>B: beritahu(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Perubahan pada peranti A memperoleh versi baharu di pelayan, dan peranti B yang menerima pemberitahuan akan mengambilnya. Pemberitahuan itu hanyalah isyarat untuk mengambil; ia tidak membawa isi kandungan.
