---
navigation:
  order: 20
---

# 1.2 Hatókör és előfeltevések

## Hatókör

| Sorszám | A hatókörbe tartozik | A hatókörön kívül esik |
|---|---|---|
| 1 | Jegyzetek létrehozásának, módosításának és törlésének szinkronizálása | Jegyzetek közös szerkesztése (egyidejű szerkesztés kurzorainak megosztása) |
| 2 | Az eszközök közötti ütközések felismerése és feloldása | Az eszközön belüli szerkesztő |
| 3 | A szinkronizálási API (HTTP) | Számlázás, fiókkezelés |

## Előfeltevések

- Az eszközök csak időszakosan kapcsolódnak. Az offline szerkesztés a szokásos eset.
- Egy jegyzet törzsének mérete legfeljebb 1 MB.
- A sorrend nem az eszközök óráitól függ: a kiszolgáló verziószámai döntik el.
