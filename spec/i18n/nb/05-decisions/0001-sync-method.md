---
navigation:
  order: 10
---

# ORB-ADR-0001: Velge «servertildelte versjoner med treveis fletting» som synkroniseringsmetode

| Element | Innhold |
|---|---|
| Dokument-ID | ORB-ADR-0001 |
| Versjon | 1.0 |
| Oppdatert | 2026-07-01 |
| Status | Godkjent |

## 1. Bakgrunn

Notater som redigeres frakoblet på flere enheter, må konvergere. Tre alternativer ble vurdert: (a) siste endringstidspunkt vinner, (b) en CRDT, (c) servertildelte versjonsnumre med treveis fletting.

## 2. Beslutning

| Nr. | Beslutning |
|---|---|
| 1 | Rekkefølgen avgjøres av versjonsnumre som serveren tildeler. Klokkene på enhetene er ikke til å stole på |
| 2 | Konflikter løses med treveis fletting, og en linje som ikke kan løses, beholder begge sider. Å ikke miste innhold har førsteprioritet |
| 3 | CRDT tas ikke i bruk. Notatene er korte, det finnes ikke noe krav om samtidig redigering, og det er ikke verdt prisen at brødteksten blir dobbelt så stor eller mer |

## 3. Konsekvenser

| Nr. | Konsekvens |
|---|---|
| 1 | Enheten holder på `baseVersion` og legger den ved hver sending |
| 2 | Visning av en konflikt (REQ-006) blir en påkrevd funksjon på enheten |
| 3 | Serveren beholder de siste 30 dagenes historikk (til papirkurven og som grunnlag for treveis fletting) |
