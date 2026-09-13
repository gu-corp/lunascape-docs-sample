---
navigation:
  order: 30
---

# 4.3 Feil

| Status | Betydning | Hva enheten gjør |
|---|---|---|
| 400 | Ugyldig format på forespørselen | Stopp sendingen, og loggfør den |
| 401 | Ugyldig token | Autentiser på nytt |
| 409 | Versjonene stemmer ikke (konflikt) | Erstatt med `body` fra svaret, og vis at det er en konflikt |
| 413 | Innholdet er over 1 MB | Gi beskjed til brukeren, og ikke send |
| 429 | For mange forespørsler | Vent det antallet sekunder som `Retry-After` angir, og send på nytt |
| 5xx | Feil på serveren | Send på nytt med eksponentiell backoff (opptil 5 ganger) |
