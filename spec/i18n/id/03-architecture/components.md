---
navigation:
  order: 10
---

# 3.1 Komponen

| Elemen | Peran |
|---|---|
| Klien | Memantau penyuntingan catatan, memasukkan perubahan ke antrean, dan mengirimkannya ke server saat terhubung |
| API Sinkronisasi | Menerima perubahan, memberi nomor versi, dan mendistribusikannya ke perangkat lain |
| Penyimpanan | Menyimpan isi terkini setiap catatan beserta riwayat 30 hari terakhir |
| Notifikasi | Mengirim sinyal ringan untuk meminta perangkat menarik data, ketika terjadi perubahan |

```mermaid
flowchart TB
  subgraph A[Perangkat A]
    EA[Editor] --> QA[Antrean]
  end
  subgraph B[Perangkat B]
    EB[Editor] --> QB[Antrean]
  end
  QA -- push --> API[API Sinkronisasi]
  QB -- push --> API
  API --> STORE[(Penyimpanan)]
  API --> NOTIFY[Notifikasi]
  NOTIFY -. meminta pull .-> QA
  NOTIFY -. meminta pull .-> QB
```
