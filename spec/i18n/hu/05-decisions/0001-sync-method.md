---
navigation:
  order: 10
---

# ORB-ADR-0001: A szinkronizálás módja „kiszolgáló által kiosztott verziók és háromutas összefésülés”

| Tétel | Tartalom |
|---|---|
| Dokumentumazonosító | ORB-ADR-0001 |
| Verzió | 1.0 |
| Frissítve | 2026-07-01 |
| Állapot | Jóváhagyva |

## 1. Háttér

A több eszközön, kapcsolat nélkül szerkesztett jegyzeteknek össze kell tartaniuk. Három lehetőség merült fel: (a) az utolsó módosítás időbélyege győz, (b) CRDT, (c) a kiszolgáló által kiosztott verziószámok háromutas összefésüléssel.

## 2. Döntés

| Sorszám | Döntés |
|---|---|
| 1 | A sorrendet a kiszolgáló által kiosztott verziószámok határozzák meg; az eszközök óráiban nem bízunk |
| 2 | Az ütközéseket háromutas összefésülés oldja fel, és amelyik sort nem lehet összefésülni, ott mindkét oldal megmarad. Az elsődleges szempont, hogy ne vesszen el tartalom |
| 3 | CRDT-t nem vezetünk be: a jegyzetek rövidek, nincs igény egyidejű szerkesztésre, és nem éri meg az az ár, hogy a törzsszöveg mérete a kétszeresére vagy annál is nagyobbra nő |

## 3. Következmények

| Sorszám | Következmény |
|---|---|
| 1 | Az eszköz megőrzi a `baseVersion` értéket, és minden küldéshez mellékeli |
| 2 | Az ütközés megjelenítése (REQ-006) kötelező eszközfunkcióvá válik |
| 3 | A kiszolgáló 30 nap előzményt tart meg (a Kuka miatt, és a háromutas összefésülések alapjaként) |
