---
navigation:
  order: 10
---

# ORB-ADR-0001: Zvolit „serverem přidělované verze s třícestným sloučením“ jako způsob synchronizace

| Položka | Obsah |
|---|---|
| ID dokumentu | ORB-ADR-0001 |
| Verze | 1.0 |
| Datum aktualizace | 2026-07-01 |
| Stav | Schváleno |

## 1. Souvislosti

Poznámky upravované offline na několika zařízeních se musí sjednotit. V úvahu přicházely tři možnosti: (a) vítězí poslední zápis podle času úpravy, (b) CRDT, (c) čísla verzí přidělovaná serverem s třícestným sloučením.

## 2. Rozhodnutí

| Č. | Rozhodnutí |
|---|---|
| 1 | Pořadí určují čísla verzí, která přiděluje server; hodinám zařízení se nedůvěřuje |
| 2 | Konflikty se řeší třícestným sloučením; řádek, který sloučit nelze, ponechá obě strany. Přednost má neztratit obsah |
| 3 | CRDT se nepoužije: poznámky jsou krátké, není požadavek na současné úpravy a dvojnásobná či větší velikost těla textu za tu cenu nestojí |

## 3. Dopady

| Č. | Dopad |
|---|---|
| 1 | Zařízení uchovává `baseVersion` a připojuje ji ke každému odeslání |
| 2 | Zobrazení konfliktu (REQ-006) se stává povinnou funkcí zařízení |
| 3 | Server uchovává historii za posledních 30 dní (pro Koš a jako základ třícestného sloučení) |
