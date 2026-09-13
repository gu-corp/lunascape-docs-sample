# Orbit jegyzetszinkronizáló szolgáltatás – funkcionális specifikáció

| Tétel | Tartalom |
|---|---|
| Dokumentumazonosító | ORB-SPEC-001 |
| Verzió | 1.3 |
| Frissítve | 2026-09-06 |
| Állapot | Jóváhagyva |
| Dokumentumgazda | Orbit fejlesztőcsapat (kitalált) |
| Kapcsolódó | ORB-REQ-001 (követelménylista), ORB-ADR-0001 (a szinkronizálási mód kiválasztása) |

## Változásnapló

| Verzió | Dátum | A változás leírása | Szerző |
|---|---|---|---|
| 1.0 | 2026-07-01 | Első kiadás | Orbit fejlesztőcsapat |
| 1.1 | 2026-08-10 | Ütközésfeloldási szabályok hozzáadva (3.4) | Orbit fejlesztőcsapat |
| 1.2 | 2026-09-06 | API-hibatáblázat hozzáadva (4.3) | Orbit fejlesztőcsapat |
| 1.3 | 2026-09-06 | Átszervezve fejezetenkénti mappákra | Orbit fejlesztőcsapat |

## Felépítés

1. [Áttekintés](01-overview/README.md) — cél, [hatókör és előfeltevések](01-overview/scope.md), [fogalmak](01-overview/terms.md)
2. [Követelmények](02-requirements/README.md) — [funkcionális követelmények](02-requirements/functional.md), [nem funkcionális követelmények](02-requirements/non-functional.md), [követelmények nyomon követése](02-requirements/traceability.md)
3. [Felépítés](03-architecture/README.md) — [összetevők](03-architecture/components.md), [a szinkronizálás menete](03-architecture/sync-flow.md), [verziószámozás](03-architecture/versioning.md), [ütközések feloldása](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [végpontok](04-api/endpoints.md), [kérés és válasz](04-api/push.md), [hibák](04-api/errors.md)
5. [Tervezési döntések](05-decisions/README.md) — [ORB-ADR-0001: a szinkronizálási mód kiválasztása](05-decisions/0001-sync-method.md)

> **Erről a dokumentumról**
> Kitalált specifikáció, amely példaként készült arra, hogyan érdemes a Lunascape Docs számára írni. Ilyen termék és cég nem létezik. Azt mutatja be, hogyan használhatók a fejezetenkénti mappák, a táblázatok, az ábrák (Mermaid), a kód és a fordítások.
