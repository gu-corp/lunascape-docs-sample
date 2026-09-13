---
navigation:
  order: 30
---

# 2.3 Pelacakan persyaratan

Persyaratan dipetakan ke setiap elemen [arsitektur](../03-architecture/README.md) dan setiap endpoint [API](../04-api/README.md). Persyaratan yang tidak memiliki pemetaan dianggap belum diimplementasikan.

```mermaid
flowchart LR
  REQ001[REQ-001 tiba dalam 10 detik] --> PUSH["/notes/push"]
  REQ002[REQ-002 dikirim saat tersambung kembali] --> QUEUE[Antrean di sisi perangkat]
  REQ003[REQ-003 deteksi konflik] --> VERSION[Pencocokan nomor versi]
  REQ004[REQ-004 penyelesaian otomatis] --> MERGE[Penggabungan tiga arah]
  QUEUE --> PUSH
  VERSION --> MERGE
```
