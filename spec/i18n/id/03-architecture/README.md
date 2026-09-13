---
navigation:
  order: 30
---

# 3. Arsitektur

Sinkronisasi terdiri atas empat elemen: klien, API sinkronisasi, penyimpanan, dan notifikasi ([komponen](components.md)). [Alur sinkronisasi](sync-flow.md) menunjukkan urutan perjalanan sebuah perubahan dari perangkat ke server, dan dari server ke perangkat lain. Dasar urutan itu adalah [nomor versi](versioning.md); penanganan dua pembaruan yang jatuh pada versi yang sama ditetapkan dalam [penyelesaian konflik](conflicts.md).
