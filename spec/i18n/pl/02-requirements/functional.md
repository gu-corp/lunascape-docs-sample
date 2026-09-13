---
navigation:
  order: 10
---

# 2.1 Wymagania funkcjonalne

| ID | Wymaganie | Priorytet | Sposób weryfikacji |
|---|---|---|---|
| REQ-001 | Notatka utworzona na jednym urządzeniu dociera do pozostałych urządzeń w ciągu 10 sekund od połączenia | Wymagane | Test integracyjny |
| REQ-002 | Notatka zmieniona w trybie offline jest wysyłana automatycznie po ponownym połączeniu | Wymagane | Test integracyjny |
| REQ-003 | Dwie aktualizacje tej samej wersji są wykrywane jako konflikt | Wymagane | Test jednostkowy |
| REQ-004 | Konflikt jest rozwiązywany automatycznie według [reguł z punktu 3.4](../03-architecture/conflicts.md), bez utraty treści żadnej ze stron | Wymagane | Test jednostkowy |
| REQ-005 | Usunięcie jest przenoszone na pozostałe urządzenia, a przez 30 dni można je przywrócić z kosza | Zalecane | Test integracyjny |
| REQ-006 | Urządzenie może pokazywać stan synchronizacji (zsynchronizowano, wysyłanie, konflikt) | Zalecane | Kontrola wzrokowa |
