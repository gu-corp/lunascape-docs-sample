---
navigation:
  order: 30
---

# 4.3 Galat

| Status | Arti | Tindakan perangkat |
|---|---|---|
| 400 | Format permintaan tidak valid | Hentikan pengiriman, lalu catat di log |
| 401 | Token tidak valid | Lakukan autentikasi ulang |
| 409 | Versi tidak cocok (konflik) | Ganti dengan `body` pada respons, lalu tampilkan adanya konflik |
| 413 | Isi melebihi 1 MB | Beri tahu pengguna, dan jangan kirim |
| 429 | Permintaan terlalu banyak | Tunggu sebanyak detik yang disebutkan pada `Retry-After`, lalu kirim ulang |
| 5xx | Gangguan pada server | Kirim ulang dengan backoff eksponensial (maksimal 5 kali) |
