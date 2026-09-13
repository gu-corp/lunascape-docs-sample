# Orbit notsynkronisering – funktionsspecifikation

| Post | Värde |
|---|---|
| Dokument-ID | ORB-SPEC-001 |
| Version | 1.3 |
| Uppdaterad | 2026-09-06 |
| Status | Godkänd |
| Dokumentansvarig | Orbit-teamet (fiktivt) |
| Relaterat | ORB-REQ-001 (kravlista), ORB-ADR-0001 (val av synkroniseringsmetod) |

## Revisionshistorik

| Version | Datum | Ändring | Författare |
|---|---|---|---|
| 1.0 | 2026-07-01 | Första utgåvan | Orbit-teamet |
| 1.1 | 2026-08-10 | Regler för konflikthantering tillagda (3.4) | Orbit-teamet |
| 1.2 | 2026-09-06 | Feltabell för API tillagd (4.3) | Orbit-teamet |
| 1.3 | 2026-09-06 | Omarbetad till en mapp per kapitel | Orbit-teamet |

## Struktur

1. [Översikt](01-overview/README.md) – syfte, [omfattning och förutsättningar](01-overview/scope.md), [termer](01-overview/terms.md)
2. [Krav](02-requirements/README.md) – [funktionella krav](02-requirements/functional.md), [icke-funktionella krav](02-requirements/non-functional.md), [kravspårning](02-requirements/traceability.md)
3. [Arkitektur](03-architecture/README.md) – [komponenter](03-architecture/components.md), [synkroniseringsflödet](03-architecture/sync-flow.md), [versionsnummer](03-architecture/versioning.md), [konflikthantering](03-architecture/conflicts.md)
4. [API](04-api/README.md) – [slutpunkter](04-api/endpoints.md), [begäran och svar](04-api/push.md), [fel](04-api/errors.md)
5. [Designbeslut](05-decisions/README.md) – [ORB-ADR-0001, val av synkroniseringsmetod](05-decisions/0001-sync-method.md)

> **Om det här dokumentet**
> En fiktiv Specifikation som skrivits som ett exempel på hur man skriver i Lunascape Docs. Produkten och företaget finns inte i verkligheten. Den visar hur en mapp per kapitel, tabeller, Diagram (Mermaid), kod och Översättning används.
