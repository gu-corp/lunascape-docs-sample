---
navigation:
  order: 30
---

# 3. Arhitektura

Sinkronizacija se sastoji od četiri elementa: klijenta, API-ja za sinkronizaciju, pohrane i obavijesti ([sastavni dijelovi](components.md)). [Tijek sinkronizacije](sync-flow.md) prikazuje redoslijed kojim promjena putuje s uređaja na poslužitelj te s poslužitelja na druge uređaje. Taj se redoslijed temelji na [brojevima verzija](versioning.md), a postupanje kada se dvije promjene odnose na istu verziju određeno je u [rješavanju sukoba](conflicts.md).
