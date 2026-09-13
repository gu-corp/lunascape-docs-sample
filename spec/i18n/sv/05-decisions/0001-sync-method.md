---
navigation:
  order: 10
---

# ORB-ADR-0001: Välj "serverstilldelade versioner med trevägssammanslagning" som synkroniseringsmetod

| Post | Innehåll |
|---|---|
| Dokument-ID | ORB-ADR-0001 |
| Version | 1.0 |
| Uppdaterad | 2026-07-01 |
| Status | Godkänd |

## 1. Bakgrund

Anteckningar som redigeras offline på flera enheter måste konvergera. Tre alternativ övervägdes: (a) senaste ändringstidpunkt vinner, (b) en CRDT, (c) serverstilldelade versionsnummer med en trevägssammanslagning.

## 2. Beslut

| Nr | Beslut |
|---|---|
| 1 | Ordningen avgörs av versionsnummer som servern tilldelar. Enheternas klockor är inte att lita på |
| 2 | Konflikter löses med en trevägssammanslagning, och en rad som inte kan lösas behåller båda sidorna. Att inte förlora innehåll går först |
| 3 | CRDT används inte: anteckningarna är korta, det finns inget krav på samtidig redigering, och att texten blir dubbelt så stor eller mer är inte värt priset |

## 3. Konsekvenser

| Nr | Konsekvens |
|---|---|
| 1 | Enheten håller `baseVersion` och bifogar det vid varje sändning |
| 2 | Att visa en konflikt (REQ-006) blir en nödvändig funktion i enheten |
| 3 | Servern har 30 dagars historik (för papperskorgen och som bas för trevägssammanslagningar) |
