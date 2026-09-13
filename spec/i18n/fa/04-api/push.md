---
navigation:
  order: 20
---

# ۴.۲ درخواست و پاسخ

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "خرید\n- شیر\n- تخم‌مرغ",
  "deviceId": "d_macbook"
}
```

پاسخ (موفق):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

پاسخ (تعارض. نتیجه‌ای که با [قواعد بخش ۳.۴](../03-architecture/conflicts.md) حل شده است بازگردانده می‌شود):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "خرید\n- شیر\n- تخم‌مرغ\n>>> d_iphone\n- نان" }
```
