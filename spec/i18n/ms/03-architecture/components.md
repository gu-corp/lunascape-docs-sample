---
navigation:
  order: 10
---

# 3.1 Komponen

| Elemen | Peranan |
|---|---|
| Klien | Memantau suntingan pada nota, membariskan perubahan dalam baris gilir, dan menghantarnya ke pelayan apabila tersambung |
| API penyegerakan | Menerima perubahan, memberikan nombor versi, dan mengedarkannya ke peranti lain |
| Stor | Menyimpan kandungan semasa setiap nota dan sejarahnya bagi 30 hari terakhir |
| Pemberitahuan | Menghantar isyarat ringan untuk menggesa peranti menarik perubahan, apabila berlaku perubahan |

```mermaid
flowchart TB
  subgraph A[Peranti A]
    EA[Penyunting] --> QA[Baris gilir]
  end
  subgraph B[Peranti B]
    EB[Penyunting] --> QB[Baris gilir]
  end
  QA -- push --> API[API penyegerakan]
  QB -- push --> API
  API --> STORE[(Stor)]
  API --> NOTIFY[Pemberitahuan]
  NOTIFY -. menggesa pull .-> QA
  NOTIFY -. menggesa pull .-> QB
```
