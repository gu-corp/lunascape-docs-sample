---
navigation:
  order: 10
---

# ORB-ADR-0001: Vælg "serverangivne versioner med trevejsfletning" som synkroniseringsmetode

| Punkt | Værdi |
|---|---|
| Dokument-ID | ORB-ADR-0001 |
| Version | 1.0 |
| Opdateret | 2026-07-01 |
| Status | Godkendt |

## 1. Baggrund

Noter, der redigeres offline på flere enheder, skal konvergere. Der var tre kandidater: (a) seneste ændringstidspunkt vinder, (b) en CRDT, (c) serverangivne versionsnumre med trevejsfletning.

## 2. Beslutning

| Nr. | Beslutning |
|---|---|
| 1 | Rækkefølgen afgøres af versionsnumre, som serveren tildeler. Enhedernes ure er der ikke tillid til |
| 2 | Konflikter løses med en trevejsfletning, og en linje, der ikke kan løses, bevarer begge sider. Det har førsteprioritet ikke at miste indhold |
| 3 | En CRDT blev ikke valgt: noterne er korte, der er ikke behov for samtidig redigering, og det er ikke prisen værd at fordoble brødtekstens størrelse eller mere |

## 3. Konsekvenser

| Nr. | Konsekvens |
|---|---|
| 1 | En enhed gemmer `baseVersion` og vedlægger den ved hver afsendelse |
| 2 | Visning af en konflikt (REQ-006) bliver en påkrævet funktion på enheden |
| 3 | Serveren gemmer de seneste 30 dages historik (til papirkurven og som grundlag for trevejsfletninger) |
