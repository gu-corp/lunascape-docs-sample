---
navigation:
  order: 20
---

# 4.2 অনুরোধ ও প্রতিক্রিয়া

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "কেনাকাটা\n- দুধ\n- ডিম",
  "deviceId": "d_macbook"
}
```

প্রতিক্রিয়া (সফল):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

প্রতিক্রিয়া (দ্বন্দ্ব। [3.4-এর নিয়ম](../03-architecture/conflicts.md) দিয়ে সমাধান করা ফলাফল ফেরত দেওয়া হয়):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "কেনাকাটা\n- দুধ\n- ডিম\n>>> d_iphone\n- পাউরুটি" }
```
