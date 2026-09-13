# Orbit Note Sync — specyfikacja funkcjonalna

| Pozycja | Wartość |
|---|---|
| ID dokumentu | ORB-SPEC-001 |
| Wersja | 1.3 |
| Data aktualizacji | 2026-09-06 |
| Stan | Zatwierdzony |
| Właściciel dokumentu | Zespół Orbit (fikcyjny) |
| Powiązania | ORB-REQ-001 (lista wymagań), ORB-ADR-0001 (wybór metody synchronizacji) |

## Historia zmian

| Wersja | Data | Opis zmiany | Autor |
|---|---|---|---|
| 1.0 | 2026-07-01 | Wydanie pierwsze | Zespół Orbit |
| 1.1 | 2026-08-10 | Dodano reguły rozwiązywania konfliktów (3.4) | Zespół Orbit |
| 1.2 | 2026-09-06 | Dodano tabelę błędów API (4.3) | Zespół Orbit |
| 1.3 | 2026-09-06 | Przebudowano na układ jednego folderu na rozdział | Zespół Orbit |

## Struktura

1. [Przegląd](01-overview/README.md) — cel, [zakres i założenia](01-overview/scope.md), [terminy](01-overview/terms.md)
2. [Wymagania](02-requirements/README.md) — [wymagania funkcjonalne](02-requirements/functional.md), [wymagania pozafunkcjonalne](02-requirements/non-functional.md), [śledzenie wymagań](02-requirements/traceability.md)
3. [Architektura](03-architecture/README.md) — [elementy składowe](03-architecture/components.md), [przebieg synchronizacji](03-architecture/sync-flow.md), [numeracja wersji](03-architecture/versioning.md), [rozwiązywanie konfliktów](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [punkty końcowe](04-api/endpoints.md), [żądanie i odpowiedź](04-api/push.md), [błędy](04-api/errors.md)
5. [Decyzje projektowe](05-decisions/README.md) — [ORB-ADR-0001 Wybór metody synchronizacji](05-decisions/0001-sync-method.md)

> **O tym dokumencie**
> To fikcyjna specyfikacja przygotowana jako przykład sposobu pisania w Lunascape Docs. Opisany produkt ani firma nie istnieją. Pokazuje ona zastosowanie folderów dla poszczególnych rozdziałów, tabel, diagramów (Mermaid), kodu i tłumaczeń.
