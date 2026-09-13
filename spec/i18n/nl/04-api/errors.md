---
navigation:
  order: 30
---

# 4.3 Fouten

| Status | Betekenis | Wat het apparaat doet |
|---|---|---|
| 400 | Onjuist opgemaakt verzoek | Stop met verzenden en leg het vast in het logboek |
| 401 | Token is ongeldig | Opnieuw verifiëren |
| 409 | Versies komen niet overeen (conflict) | Vervang door de `body` van het antwoord en toon een conflict |
| 413 | Inhoud groter dan 1 MB | Meld dit aan de gebruiker en verzend niet |
| 429 | Te veel verzoeken | Wacht het aantal seconden uit `Retry-After` en verzend opnieuw |
| 5xx | Storing op de server | Verzend opnieuw met exponentiële uitstelduur (maximaal 5 keer) |
