# Orbit — synchronizace poznámek: funkční specifikace

| Položka | Obsah |
|---|---|
| ID dokumentu | ORB-SPEC-001 |
| Verze | 1.3 |
| Datum aktualizace | 2026-09-06 |
| Stav | Schváleno |
| Vlastník dokumentu | Vývojový tým Orbit (fiktivní) |
| Související | ORB-REQ-001 (seznam požadavků), ORB-ADR-0001 (volba způsobu synchronizace) |

## Historie revizí

| Verze | Datum | Obsah revize | Autor revize |
|---|---|---|---|
| 1.0 | 2026-07-01 | První vydání | Vývojový tým Orbit |
| 1.1 | 2026-08-10 | Doplněna pravidla řešení konfliktů (3.4) | Vývojový tým Orbit |
| 1.2 | 2026-09-06 | Doplněna tabulka chyb API (4.3) | Vývojový tým Orbit |
| 1.3 | 2026-09-06 | Přepracováno na jednu složku pro každou kapitolu | Vývojový tým Orbit |

## Struktura

1. [Přehled](01-overview/README.md) — účel, [rozsah a předpoklady](01-overview/scope.md), [pojmy](01-overview/terms.md)
2. [Požadavky](02-requirements/README.md) — [funkční požadavky](02-requirements/functional.md), [nefunkční požadavky](02-requirements/non-functional.md), [sledování požadavků](02-requirements/traceability.md)
3. [Architektura](03-architecture/README.md) — [součásti](03-architecture/components.md), [průběh synchronizace](03-architecture/sync-flow.md), [číslování verzí](03-architecture/versioning.md), [řešení konfliktů](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [koncové body](04-api/endpoints.md), [požadavek a odpověď](04-api/push.md), [chyby](04-api/errors.md)
5. [Rozhodnutí](05-decisions/README.md) — [ORB-ADR-0001 Volba způsobu synchronizace](05-decisions/0001-sync-method.md)

> **O tomto dokumentu**
> Fiktivní specifikace vytvořená jako ukázka toho, jak se v Lunascape Docs píše. Uvedený produkt ani společnost neexistují. Slouží k předvedení složek podle kapitol, tabulek, diagramů (Mermaid), kódu a překladů.
