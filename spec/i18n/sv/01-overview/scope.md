---
navigation:
  order: 20
---

# 1.2 Omfattning och antaganden

## Omfattning

| Nr | Ingår | Ingår inte |
|---|---|---|
| 1 | Synkronisering av att anteckningar skapas, uppdateras och tas bort | Samtidig redigering av anteckningar (delade markörer) |
| 2 | Upptäckt och lösning av konflikter mellan enheter | Redigeraren på enheten |
| 3 | Synkroniserings-API:et (HTTP) | Betalning och kontohantering |

## Antaganden

- Enheterna är bara anslutna periodvis. Redigering offline är utgångspunkten.
- En antecknings brödtext är högst 1 MB.
- Ordningen beror inte på enheternas klockor; serverns versionsnummer avgör den.
