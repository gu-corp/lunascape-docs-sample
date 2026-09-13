# Funkcijska specifikacija servisa za sinkronizaciju bilježaka Orbit

| Stavka | Sadržaj |
|---|---|
| ID dokumenta | ORB-SPEC-001 |
| Izdanje | 1.3 |
| Datum izmjene | 2026-09-06 |
| Status | Odobreno |
| Vlasnik dokumenta | Razvojni tim Orbit (izmišljen) |
| Povezano | ORB-REQ-001 (popis zahtjeva), ORB-ADR-0001 (izbor načina sinkronizacije) |

## Povijest izmjena

| Izdanje | Datum | Sadržaj izmjene | Autor izmjene |
|---|---|---|---|
| 1.0 | 2026-07-01 | Prvo izdanje | Razvojni tim Orbit |
| 1.1 | 2026-08-10 | Dodana pravila za rješavanje sukoba (3.4) | Razvojni tim Orbit |
| 1.2 | 2026-09-06 | Dodana tablica pogrešaka za API (4.3) | Razvojni tim Orbit |
| 1.3 | 2026-09-06 | Preuređeno u jednu mapu po poglavlju | Razvojni tim Orbit |

## Ustroj

1. [Pregled](01-overview/README.md) — svrha, [opseg i pretpostavke](01-overview/scope.md), [pojmovi](01-overview/terms.md)
2. [Zahtjevi](02-requirements/README.md) — [funkcijski zahtjevi](02-requirements/functional.md), [nefunkcijski zahtjevi](02-requirements/non-functional.md), [praćenje zahtjeva](02-requirements/traceability.md)
3. [Ustroj](03-architecture/README.md) — [sastavni dijelovi](03-architecture/components.md), [tijek sinkronizacije](03-architecture/sync-flow.md), [brojevi izdanja](03-architecture/versioning.md), [rješavanje sukoba](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [krajnje točke](04-api/endpoints.md), [zahtjev i odgovor](04-api/push.md), [pogreške](04-api/errors.md)
5. [Odluke o dizajnu](05-decisions/README.md) — [ORB-ADR-0001 izbor načina sinkronizacije](05-decisions/0001-sync-method.md)

> **O ovom dokumentu**
> Ovo je izmišljena Specifikacija napisana kao primjer načina pisanja u Lunascape Docs. Takav proizvod i tvrtka ne postoje. Služi za prikaz mapa po poglavljima, tablica, dijagrama (Mermaid), koda i prijevoda u uporabi.
