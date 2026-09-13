---
navigation:
  order: 10
---

# 2.1 Persyaratan fungsional

| ID | Persyaratan | Prioritas | Metode verifikasi |
|---|---|---|---|
| REQ-001 | Catatan yang dibuat di satu perangkat sampai ke perangkat lain dalam 10 detik setelah tersambung | Wajib | Uji integrasi |
| REQ-002 | Catatan yang disunting secara luring dikirim otomatis saat tersambung kembali | Wajib | Uji integrasi |
| REQ-003 | Dua pembaruan pada versi yang sama terdeteksi sebagai konflik | Wajib | Uji unit |
| REQ-004 | Konflik diselesaikan otomatis dengan [aturan pada 3.4](../03-architecture/conflicts.md), tanpa kehilangan isi dari kedua sisi | Wajib | Uji unit |
| REQ-005 | Penghapusan diteruskan ke perangkat lain, dan dapat dipulihkan dari tempat sampah selama 30 hari | Disarankan | Uji integrasi |
| REQ-006 | Perangkat dapat menampilkan status sinkronisasi (tersinkron, sedang mengirim, ada konflik) | Disarankan | Pemeriksaan visual |
