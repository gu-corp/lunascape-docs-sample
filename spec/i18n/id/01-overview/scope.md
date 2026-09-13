---
navigation:
  order: 20
---

# 1.2 Ruang lingkup dan asumsi

## Ruang lingkup

| No. | Termasuk ruang lingkup | Di luar ruang lingkup |
|---|---|---|
| 1 | Sinkronisasi pembuatan, pembaruan, dan penghapusan catatan | Penyuntingan catatan secara bersama (berbagi kursor saat menyunting bersamaan) |
| 2 | Deteksi dan penyelesaian konflik antarperangkat | Editor di dalam perangkat |
| 3 | API sinkronisasi (HTTP) | Penagihan dan pengelolaan akun |

## Asumsi

- Perangkat hanya terhubung secara terputus-putus. Penyuntingan luring diasumsikan sebagai hal yang biasa.
- Batas atas isi sebuah catatan adalah 1 MB.
- Urutan tidak bergantung pada jam perangkat, melainkan ditentukan oleh nomor versi dari server.
