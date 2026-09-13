---
navigation:
  order: 30
---

# 4.3 Fejl

| Status | Betydning | Hvad enheden gør |
|---|---|---|
| 400 | Forkert udformet anmodning | Stop afsendelsen, og skriv det i loggen |
| 401 | Ugyldigt token | Godkend igen |
| 409 | Versionerne stemmer ikke (konflikt) | Erstat med svarets `body`, og vis, at der er en konflikt |
| 413 | Indholdet er over 1 MB | Sig det til brugeren, og send ikke |
| 429 | For mange anmodninger | Vent det antal sekunder, `Retry-After` angiver, og send igen |
| 5xx | Serverfejl | Send igen med eksponentiel backoff (højst 5 gange) |
