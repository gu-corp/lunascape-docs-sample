---
navigation:
  order: 30
---

# 3.3 Numery wersji

Numer wersji to monotonicznie rosnąca liczba całkowita, którą serwer przydziela osobno dla każdej notatki. Urządzenie wysyła ostatnią otrzymaną wersję jako `baseVersion`. Gdy bieżąca wersja na serwerze nie zgadza się z `baseVersion`, oznacza to konflikt (REQ-003). Zegary urządzeń nie biorą udziału w ustalaniu kolejności ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
