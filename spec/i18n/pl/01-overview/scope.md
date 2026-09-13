---
navigation:
  order: 20
---

# 1.2 Zakres i założenia

## Zakres

| Lp. | W zakresie | Poza zakresem |
|---|---|---|
| 1 | Synchronizacja tworzenia, aktualizacji i usuwania notatek | Wspólna edycja notatek (współdzielenie kursorów przy jednoczesnej edycji) |
| 2 | Wykrywanie i rozwiązywanie konfliktów między urządzeniami | Edytor na urządzeniu |
| 3 | API synchronizacji (HTTP) | Płatności, zarządzanie kontem |

## Założenia

- Urządzenia łączą się tylko z przerwami. Zakładamy edycję w trybie offline.
- Treść notatki ma maksymalnie 1 MB.
- Kolejność nie zależy od zegara urządzenia; decydują o niej numery wersji nadawane przez serwer.
