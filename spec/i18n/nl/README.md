# Orbit Note Sync — Functionele specificatie

| Item | Waarde |
|---|---|
| Document-ID | ORB-SPEC-001 |
| Versie | 1.3 |
| Bijgewerkt op | 2026-09-06 |
| Status | Goedgekeurd |
| Documenteigenaar | Orbit-ontwikkelteam (fictief) |
| Gerelateerd | ORB-REQ-001 (overzicht van de eisen), ORB-ADR-0001 (keuze van de synchronisatiemethode) |

## Revisiegeschiedenis

| Versie | Datum | Wijziging | Auteur |
|---|---|---|---|
| 1.0 | 2026-07-01 | Eerste versie | Orbit-ontwikkelteam |
| 1.1 | 2026-08-10 | Regels voor conflictoplossing toegevoegd (3.4) | Orbit-ontwikkelteam |
| 1.2 | 2026-09-06 | Fouttabel van de API toegevoegd (4.3) | Orbit-ontwikkelteam |
| 1.3 | 2026-09-06 | Herzien naar één map per hoofdstuk | Orbit-ontwikkelteam |

## Opbouw

1. [Overzicht](01-overview/README.md) — doel, [reikwijdte en aannames](01-overview/scope.md), [termen](01-overview/terms.md)
2. [Eisen](02-requirements/README.md) — [functionele eisen](02-requirements/functional.md), [niet-functionele eisen](02-requirements/non-functional.md), [traceerbaarheid van de eisen](02-requirements/traceability.md)
3. [Architectuur](03-architecture/README.md) — [onderdelen](03-architecture/components.md), [het verloop van de synchronisatie](03-architecture/sync-flow.md), [versienummers](03-architecture/versioning.md), [conflictoplossing](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [eindpunten](04-api/endpoints.md), [aanvraag en antwoord](04-api/push.md), [fouten](04-api/errors.md)
5. [Ontwerpbeslissingen](05-decisions/README.md) — [ORB-ADR-0001, de keuze van de synchronisatiemethode](05-decisions/0001-sync-method.md)

> **Over dit document**
> Een fictieve specificatie, geschreven als voorbeeld van de schrijfwijze van Lunascape Docs. Het product en het bedrijf bestaan niet. Het laat zien hoe u één map per hoofdstuk, tabellen, diagrammen (Mermaid), code en vertalingen gebruikt.
