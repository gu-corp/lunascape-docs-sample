---
navigation:
  order: 30
---

# 4.3 Błędy

| Status | Znaczenie | Działanie urządzenia |
|---|---|---|
| 400 | Nieprawidłowy format żądania | Przerwij wysyłanie i zapisz w dzienniku |
| 401 | Nieważny token | Uwierzytelnij ponownie |
| 409 | Niezgodność wersji (konflikt) | Zastąp zawartością `body` z odpowiedzi i pokaż konflikt |
| 413 | Treść przekracza 1 MB | Powiadom użytkownika i nie wysyłaj |
| 429 | Zbyt wiele żądań | Odczekaj liczbę sekund podaną w `Retry-After` i wyślij ponownie |
| 5xx | Awaria serwera | Wyślij ponownie z wykładniczym odstępem (maksymalnie 5 razy) |
