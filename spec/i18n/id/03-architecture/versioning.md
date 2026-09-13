---
navigation:
  order: 30
---

# 3.3 Nomor versi

Nomor versi adalah bilangan bulat yang meningkat secara monoton dan diberikan oleh server untuk setiap catatan. Perangkat mengirimkan versi terakhir yang diterimanya sebagai `baseVersion`. Bila versi terkini di server tidak cocok dengan `baseVersion`, hal itu dianggap konflik (REQ-003). Jam pada perangkat tidak digunakan untuk menentukan urutan ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
