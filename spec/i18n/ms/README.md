# Perkhidmatan Penyegerakan Nota Orbit — Spesifikasi Fungsian

| Perkara | Kandungan |
|---|---|
| ID dokumen | ORB-SPEC-001 |
| Versi | 1.3 |
| Tarikh kemas kini | 2026-09-06 |
| Status | Diluluskan |
| Pemilik dokumen | Pasukan pembangunan Orbit (rekaan) |
| Berkaitan | ORB-REQ-001 (senarai keperluan), ORB-ADR-0001 (pemilihan kaedah penyegerakan) |

## Sejarah semakan

| Versi | Tarikh | Kandungan semakan | Penyemak |
|---|---|---|---|
| 1.0 | 2026-07-01 | Edisi pertama | Pasukan pembangunan Orbit |
| 1.1 | 2026-08-10 | Peraturan penyelesaian konflik ditambah (3.4) | Pasukan pembangunan Orbit |
| 1.2 | 2026-09-06 | Jadual ralat API ditambah (4.3) | Pasukan pembangunan Orbit |
| 1.3 | 2026-09-06 | Disusun semula kepada satu folder bagi setiap bab | Pasukan pembangunan Orbit |

## Struktur

1. [Gambaran keseluruhan](01-overview/README.md) — tujuan, [skop dan andaian](01-overview/scope.md), [istilah](01-overview/terms.md)
2. [Keperluan](02-requirements/README.md) — [keperluan fungsian](02-requirements/functional.md), [keperluan bukan fungsian](02-requirements/non-functional.md), [penjejakan keperluan](02-requirements/traceability.md)
3. [Seni bina](03-architecture/README.md) — [komponen](03-architecture/components.md), [aliran penyegerakan](03-architecture/sync-flow.md), [nombor versi](03-architecture/versioning.md), [penyelesaian konflik](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [titik akhir](04-api/endpoints.md), [permintaan dan respons](04-api/push.md), [ralat](04-api/errors.md)
5. [Keputusan reka bentuk](05-decisions/README.md) — [ORB-ADR-0001 Pemilihan kaedah penyegerakan](05-decisions/0001-sync-method.md)

> **Tentang dokumen ini**
> Spesifikasi rekaan yang dibuat sebagai contoh cara menulis dengan Lunascape Docs. Produk dan syarikat ini tidak wujud. Tujuannya adalah untuk menunjukkan penggunaan folder bagi setiap bab, jadual, rajah (Mermaid), kod dan terjemahan.
