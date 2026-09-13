---
navigation:
  order: 30
---

# 4.3 Ralat

| Status | Maksud | Tindakan peranti |
|---|---|---|
| 400 | Format permintaan tidak sah | Berhenti menghantar dan catatkan dalam log |
| 401 | Token tidak sah | Sahkan semula |
| 409 | Versi tidak sepadan (konflik) | Gantikan dengan `body` daripada respons dan paparkan konflik |
| 413 | Badan melebihi 1 MB | Beritahu pengguna dan jangan hantar |
| 429 | Terlalu banyak permintaan | Tunggu bilangan saat dalam `Retry-After`, kemudian hantar semula |
| 5xx | Kegagalan pelayan | Hantar semula dengan backoff eksponen (maksimum 5 kali) |
