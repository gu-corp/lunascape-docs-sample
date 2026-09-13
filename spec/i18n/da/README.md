# Orbit Note Sync — funktionsspecifikation

| Punkt | Værdi |
|---|---|
| Dokument-ID | ORB-SPEC-001 |
| Version | 1.3 |
| Opdateret | 2026-09-06 |
| Status | Godkendt |
| Dokumentansvarlig | Orbit-teamet (fiktivt) |
| Relateret | ORB-REQ-001 (kravliste), ORB-ADR-0001 (valg af synkroniseringsmetode) |

## Revisionshistorik

| Version | Dato | Ændring | Forfatter |
|---|---|---|---|
| 1.0 | 2026-07-01 | Første udgave | Orbit-teamet |
| 1.1 | 2026-08-10 | Regler for konfliktløsning tilføjet (3.4) | Orbit-teamet |
| 1.2 | 2026-09-06 | Fejltabel for API tilføjet (4.3) | Orbit-teamet |
| 1.3 | 2026-09-06 | Omlagt til én mappe pr. kapitel | Orbit-teamet |

## Opbygning

1. [Oversigt](01-overview/README.md) — formål, [omfang og forudsætninger](01-overview/scope.md), [termer](01-overview/terms.md)
2. [Krav](02-requirements/README.md) — [funktionelle krav](02-requirements/functional.md), [ikke-funktionelle krav](02-requirements/non-functional.md), [sporing af krav](02-requirements/traceability.md)
3. [Arkitektur](03-architecture/README.md) — [komponenter](03-architecture/components.md), [synkroniseringsforløbet](03-architecture/sync-flow.md), [versionsnumre](03-architecture/versioning.md), [konfliktløsning](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [endepunkter](04-api/endpoints.md), [forespørgsel og svar](04-api/push.md), [fejl](04-api/errors.md)
5. [Designbeslutninger](05-decisions/README.md) — [ORB-ADR-0001, valg af synkroniseringsmetode](05-decisions/0001-sync-method.md)

> **Om dette dokument**
> En fiktiv specifikation, skrevet som eksempel på, hvordan man skriver i Lunascape Docs. Produktet og virksomheden findes ikke. Den viser brugen af én mappe pr. kapitel, tabeller, diagrammer (Mermaid), kode og oversættelse.
