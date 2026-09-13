---
navigation:
  order: 10
---

# ORB-ADR-0001: Synchronisatiemethode wordt "door de server toegekende versies met driewegsamenvoeging"

| Item | Waarde |
|---|---|
| Document-ID | ORB-ADR-0001 |
| Versie | 1.0 |
| Bijgewerkt op | 2026-07-01 |
| Status | Goedgekeurd |

## 1. Achtergrond

Notities die offline op meerdere apparaten worden bewerkt, moeten naar elkaar toe convergeren. Er waren drie kandidaten: (a) de laatste wijziging op tijdstempel wint, (b) een CRDT, (c) door de server toegekende versienummers met een driewegsamenvoeging.

## 2. Besluit

| Nr. | Besluit |
|---|---|
| 1 | De volgorde wordt bepaald door versienummers die de server toekent. De klok van het apparaat wordt niet vertrouwd |
| 2 | Conflicten worden opgelost met een driewegsamenvoeging; een regel die niet kan worden samengevoegd, behoudt beide kanten. Geen inhoud verliezen heeft voorrang |
| 3 | Een CRDT wordt niet gebruikt: notities zijn kort, er is geen behoefte aan gelijktijdig bewerken, en een tekst die twee keer zo groot of groter wordt, weegt niet op tegen die kosten |

## 3. Gevolgen

| Nr. | Gevolg |
|---|---|
| 1 | Een apparaat bewaart `baseVersion` en voegt die bij elke verzending toe |
| 2 | Het tonen van een conflict (REQ-006) wordt een verplichte functie van het apparaat |
| 3 | De server bewaart 30 dagen geschiedenis (voor de Prullenbak en als basis voor driewegsamenvoegingen) |
