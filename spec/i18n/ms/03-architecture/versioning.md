---
navigation:
  order: 30
---

# 3.3 Nombor versi

Nombor versi ialah integer yang meningkat secara monoton dan diberikan oleh pelayan bagi setiap nota. Peranti menghantar versi terakhir yang diterimanya sebagai `baseVersion`. Apabila versi semasa pada pelayan tidak sepadan dengan `baseVersion`, keadaan itu ialah konflik (REQ-003). Jam peranti tidak digunakan untuk menentukan susunan ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
