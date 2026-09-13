---
navigation:
  order: 40
---

# 3.4 Rozwiązywanie konfliktów

| Przypadek | Reguła |
|---|---|
| Ten sam wiersz zmieniono niezależnie | Obie zmiany zostają zachowane: ta, która dotarła później, zostaje dopisana na końcu i oddzielona znakami `>>>`. Użytkownik widzi informację o konflikcie (REQ-006) |
| Zmieniono różne wiersze | Scalane automatycznie przez scalanie trójstronne. Użytkownik nie jest o tym informowany |
| Jedna strona usunęła notatkę | Usunięcie ma pierwszeństwo, a treść drugiej strony trafia do kosza (REQ-005) |

W żadnym przypadku treść nie zostaje utracona (REQ-004).
