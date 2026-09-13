---
navigation:
  order: 40
---

# 3.4 Řešení konfliktů

| Případ | Pravidlo |
|---|---|
| Stejný řádek byl změněn nezávisle na dvou místech | Obě změny se zachovají: ta, která dorazila později, se připojí na konec a oddělí se pomocí `>>>`. Uživateli se zobrazí konflikt (REQ-006) |
| Byly změněny různé řádky | Sloučí se automaticky trojcestným sloučením; uživateli se nic neoznamuje |
| Jedna strana záznam smazala | Smazání má přednost a obsah druhé strany se přesune do koše (REQ-005) |

V žádném z těchto případů se obsah neztratí (REQ-004).
