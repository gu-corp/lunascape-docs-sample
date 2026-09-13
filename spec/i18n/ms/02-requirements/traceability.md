---
navigation:
  order: 30
---

# 2.3 Penjejakan keperluan

Setiap keperluan dipetakan kepada elemen [seni bina](../03-architecture/README.md) dan titik akhir [API](../04-api/README.md). Keperluan yang tiada pemetaan dianggap belum dilaksanakan.

```mermaid
flowchart LR
  REQ001[REQ-001 tiba dalam masa 10 saat] --> PUSH["/notes/push"]
  REQ002[REQ-002 dihantar semasa sambung semula] --> QUEUE[Baris gilir pada peranti]
  REQ003[REQ-003 pengesanan konflik] --> VERSION[Semakan nombor versi]
  REQ004[REQ-004 penyelesaian automatik] --> MERGE[Cantuman tiga hala]
  QUEUE --> PUSH
  VERSION --> MERGE
```
