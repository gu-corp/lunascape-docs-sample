---
navigation:
  order: 30
---

# 4.3 Chyby

| Stav | Význam | Co udělá zařízení |
|---|---|---|
| 400 | Chybný formát požadavku | Přestat odesílat a zaznamenat do protokolu |
| 401 | Neplatný token | Znovu se ověřit |
| 409 | Neshoda verzí (konflikt) | Nahradit obsahem `body` z odpovědi a zobrazit konflikt |
| 413 | Tělo přesahuje 1 MB | Upozornit uživatele a neodesílat |
| 429 | Příliš mnoho požadavků | Počkat počet sekund uvedený v `Retry-After` a odeslat znovu |
| 5xx | Selhání serveru | Odeslat znovu s exponenciálním odstupem (nejvýše 5krát) |
