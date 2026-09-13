# Orbit notatsynkronisering – funksjonsspesifikasjon

| Element | Verdi |
|---|---|
| Dokument-ID | ORB-SPEC-001 |
| Versjon | 1.3 |
| Oppdatert | 2026-09-06 |
| Status | Godkjent |
| Dokumentansvarlig | Orbit-teamet (fiktivt) |
| Relatert | ORB-REQ-001 (kravliste), ORB-ADR-0001 (valg av synkroniseringsmetode) |

## Revisjonshistorikk

| Versjon | Dato | Endring | Forfatter |
|---|---|---|---|
| 1.0 | 2026-07-01 | Første utgave | Orbit-teamet |
| 1.1 | 2026-08-10 | Regler for konfliktløsning lagt til (3.4) | Orbit-teamet |
| 1.2 | 2026-09-06 | Feiltabell for API lagt til (4.3) | Orbit-teamet |
| 1.3 | 2026-09-06 | Omorganisert til én mappe per kapittel | Orbit-teamet |

## Oppbygning

1. [Oversikt](01-overview/README.md) – formål, [omfang og forutsetninger](01-overview/scope.md), [termer](01-overview/terms.md)
2. [Krav](02-requirements/README.md) – [funksjonelle krav](02-requirements/functional.md), [ikke-funksjonelle krav](02-requirements/non-functional.md), [sporing av krav](02-requirements/traceability.md)
3. [Arkitektur](03-architecture/README.md) – [komponenter](03-architecture/components.md), [synkroniseringsflyten](03-architecture/sync-flow.md), [versjonsnummer](03-architecture/versioning.md), [konfliktløsning](03-architecture/conflicts.md)
4. [API](04-api/README.md) – [endepunkter](04-api/endpoints.md), [forespørsel og svar](04-api/push.md), [feil](04-api/errors.md)
5. [Beslutninger](05-decisions/README.md) – [ORB-ADR-0001, valg av synkroniseringsmetode](05-decisions/0001-sync-method.md)

> **Om dette dokumentet**
> En fiktiv spesifikasjon laget som eksempel på hvordan man skriver i Lunascape Docs. Produktet og selskapet finnes ikke. Den viser bruk av én mappe per kapittel, tabeller, diagrammer (Mermaid), kode og oversettelser.
