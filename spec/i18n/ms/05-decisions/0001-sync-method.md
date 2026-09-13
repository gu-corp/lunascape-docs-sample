---
navigation:
  order: 10
---

# ORB-ADR-0001: Menetapkan kaedah penyegerakan sebagai "versi bernombor oleh pelayan dengan cantuman tiga hala"

| Perkara | Kandungan |
|---|---|
| ID Dokumen | ORB-ADR-0001 |
| Versi | 1.0 |
| Tarikh kemas kini | 2026-07-01 |
| Status | Diluluskan |

## 1. Latar belakang

Nota yang disunting di luar talian pada beberapa peranti perlu ditumpukan menjadi satu. Terdapat tiga calon: (a) kemas kini terakhir menang mengikut cap masa, (b) CRDT, (c) nombor versi yang dinomborkan oleh pelayan dengan cantuman tiga hala.

## 2. Keputusan

| Bil. | Perkara yang diputuskan |
|---|---|
| 1 | Susunan ditentukan oleh nombor versi yang dinomborkan oleh pelayan. Jam peranti tidak dipercayai |
| 2 | Konflik diselesaikan dengan cantuman tiga hala, dan baris yang tidak dapat diselesaikan mengekalkan kedua-dua belah. Keutamaan diberikan kepada tidak kehilangan kandungan |
| 3 | CRDT tidak digunakan. Nota adalah pendek, tiada keperluan untuk suntingan serentak, dan ia tidak berbaloi dengan kos saiz teks yang menjadi dua kali ganda atau lebih |

## 3. Kesan

| Bil. | Kesan |
|---|---|
| 1 | Peranti menyimpan `baseVersion` dan menyertakannya pada setiap penghantaran |
| 2 | Paparan konflik (REQ-006) menjadi ciri wajib pada peranti |
| 3 | Pelayan menyimpan sejarah 30 hari terkini (untuk tong sampah dan sebagai asas cantuman tiga hala) |
