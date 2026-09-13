---
navigation:
  order: 10
---

# 4.1 Endpoint

| Metode | Path | Tujuan | Persyaratan |
|---|---|---|---|
| POST | `/notes/push` | Mengirim perubahan pada catatan | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Menerima perubahan setelah versi yang ditentukan | REQ-001 |
| DELETE | `/notes/{id}` | Menghapus catatan (ke tempat sampah) | REQ-005 |
| POST | `/notes/{id}/restore` | Mengembalikan catatan dari tempat sampah | REQ-005 |
