---
navigation:
  order: 40
---

# 3.4 Penyelesaian konflik

| Kasus | Aturan |
|---|---|
| Baris yang sama diubah secara terpisah | Kedua perubahan dipertahankan: perubahan yang datang belakangan ditambahkan di akhir, dipisahkan dengan `>>>`. Perangkat menampilkan adanya konflik kepada pengguna (REQ-006) |
| Baris yang berbeda diubah | Digabungkan secara otomatis dengan penggabungan tiga arah; pengguna tidak diberi tahu |
| Salah satu pihak menghapus | Penghapusan diutamakan, dan isi dari pihak lainnya dimasukkan ke tempat sampah (REQ-005) |

Dalam setiap kasus, tidak ada isi yang hilang (REQ-004).
