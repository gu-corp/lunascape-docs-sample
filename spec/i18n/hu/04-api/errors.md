---
navigation:
  order: 30
---

# 4.3 Hibák

| Állapot | Jelentés | A készülék teendője |
|---|---|---|
| 400 | Hibás formátumú kérés | Hagyja abba a küldést, és naplózza |
| 401 | Érvénytelen token | Hitelesítsen újra |
| 409 | Verzióeltérés (ütközés) | Cserélje le a válasz `body` mezőjére, és jelezze az ütközést |
| 413 | A törzs meghaladja az 1 MB-ot | Értesítse a felhasználót, és ne küldje el |
| 429 | Túl sok kérés | Várja ki a `Retry-After` szerinti másodperceket, majd küldje újra |
| 5xx | Kiszolgálóhiba | Küldje újra exponenciális várakozással (legfeljebb 5 alkalommal) |
