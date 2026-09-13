---
navigation:
  order: 10
---

# 4.1 Titik akhir

| Kaedah | Laluan | Tujuan | Keperluan |
|---|---|---|---|
| POST | `/notes/push` | Menghantar perubahan pada nota | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Menerima perubahan selepas versi yang ditetapkan | REQ-001 |
| DELETE | `/notes/{id}` | Memadamkan nota (ke tong sampah) | REQ-005 |
| POST | `/notes/{id}/restore` | Memulihkan nota dari tong sampah | REQ-005 |
