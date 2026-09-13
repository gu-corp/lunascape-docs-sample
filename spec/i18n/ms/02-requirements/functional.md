---
navigation:
  order: 10
---

# 2.1 Keperluan fungsian

| ID | Keperluan | Keutamaan | Kaedah pengesahan |
|---|---|---|---|
| REQ-001 | Nota yang dibuat pada sesebuah peranti sampai ke peranti lain dalam masa 10 saat selepas sambungan terjalin | Wajib | Ujian integrasi |
| REQ-002 | Nota yang disunting di luar talian dihantar secara automatik apabila sambungan pulih | Wajib | Ujian integrasi |
| REQ-003 | Dua kemas kini pada versi yang sama dikesan sebagai konflik | Wajib | Ujian unit |
| REQ-004 | Konflik diselesaikan secara automatik mengikut [peraturan dalam 3.4](../03-architecture/conflicts.md), tanpa kehilangan kandungan mana-mana pihak | Wajib | Ujian unit |
| REQ-005 | Pemadaman turut ditunjukkan pada peranti lain, dan boleh dipulihkan daripada tong sampah selama 30 hari | Disyorkan | Ujian integrasi |
| REQ-006 | Peranti boleh memaparkan status penyegerakan (telah disegerak, sedang dihantar, ada konflik) | Disyorkan | Pemeriksaan visual |
