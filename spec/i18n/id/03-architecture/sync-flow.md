---
navigation:
  order: 20
---

# 3.2 Alur sinkronisasi

```mermaid
sequenceDiagram
  participant A as Perangkat A
  participant S as API Sinkronisasi
  participant B as Perangkat B
  A->>S: push(note, baseVersion=4)
  S->>S: memberi nomor versi 5
  S-->>A: 200 {version: 5}
  S-->>B: notifikasi(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

Perubahan pada perangkat A memperoleh versi baru di server, lalu perangkat B yang menerima notifikasi mengambilnya. Notifikasi hanyalah isyarat untuk mengambil; notifikasi tidak membawa isi dokumen.
