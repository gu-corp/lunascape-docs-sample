---
navigation:
  order: 30
---

# 4.3 Fel

| Status | Betydelse | Vad enheten gör |
|---|---|---|
| 400 | Felaktigt utformad begäran | Sluta skicka och logga det |
| 401 | Ogiltig token | Autentisera på nytt |
| 409 | Versionskonflikt (konflikt) | Ersätt med svarets `body` och visa en konflikt |
| 413 | Brödtexten överstiger 1 MB | Meddela användaren och skicka inte |
| 429 | För många begäranden | Vänta det antal sekunder som anges i `Retry-After` och skicka igen |
| 5xx | Serverfel | Skicka igen med exponentiell backoff (högst 5 gånger) |
