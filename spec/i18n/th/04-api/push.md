---
navigation:
  order: 20
---

# 4.2 คำขอและการตอบกลับ

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "รายการซื้อของ\n- นม\n- ไข่",
  "deviceId": "d_macbook"
}
```

การตอบกลับ (สำเร็จ):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

การตอบกลับ (ขัดแย้ง — ส่งคืนผลลัพธ์ที่แก้ไขตาม[กฎในข้อ 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "รายการซื้อของ\n- นม\n- ไข่\n>>> d_iphone\n- ขนมปัง" }
```
