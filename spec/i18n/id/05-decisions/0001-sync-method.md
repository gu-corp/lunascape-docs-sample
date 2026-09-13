---
navigation:
  order: 10
---

# ORB-ADR-0001: Menetapkan metode sinkronisasi sebagai "versi bernomor dari server dengan penggabungan tiga arah"

| Butir | Isi |
|---|---|
| ID dokumen | ORB-ADR-0001 |
| Versi | 1.0 |
| Tanggal pembaruan | 2026-07-01 |
| Status | Disetujui |

## 1. Latar belakang

Catatan yang disunting secara luring di beberapa perangkat perlu dikonvergensikan. Ada tiga kandidat: (a) penulisan terakhir menang berdasarkan waktu pembaruan, (b) CRDT, (c) nomor versi yang diberikan server dengan penggabungan tiga arah.

## 2. Keputusan

| No. | Keputusan |
|---|---|
| 1 | Urutan ditentukan oleh nomor versi yang diberikan server. Jam perangkat tidak dipercaya |
| 2 | Konflik diselesaikan dengan penggabungan tiga arah; baris yang tidak dapat diselesaikan menyimpan kedua sisinya. Tidak kehilangan isi menjadi prioritas |
| 3 | CRDT tidak diadopsi. Catatan bersifat pendek, tidak ada kebutuhan penyuntingan serentak, dan ukuran isi yang menjadi dua kali lipat atau lebih tidak sepadan dengan biayanya |

## 3. Dampak

| No. | Dampak |
|---|---|
| 1 | Perangkat menyimpan `baseVersion` dan menyertakannya pada setiap pengiriman |
| 2 | Menampilkan konflik (REQ-006) menjadi fitur wajib pada perangkat |
| 3 | Server menyimpan riwayat 30 hari terakhir (untuk tempat sampah dan sebagai dasar penggabungan tiga arah) |
