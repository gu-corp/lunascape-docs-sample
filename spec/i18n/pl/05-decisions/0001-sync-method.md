---
navigation:
  order: 10
---

# ORB-ADR-0001: Wybór metody synchronizacji „wersje nadawane przez serwer i scalanie trójstronne”

| Pozycja | Treść |
|---|---|
| Identyfikator dokumentu | ORB-ADR-0001 |
| Wersja | 1.0 |
| Data aktualizacji | 2026-07-01 |
| Stan | Zatwierdzone |

## 1. Kontekst

Notatki edytowane w trybie offline na wielu urządzeniach muszą się uzgadniać. Rozważono trzy warianty: (a) wygrywa ostatni zapis według czasu modyfikacji, (b) CRDT, (c) numery wersji nadawane przez serwer i scalanie trójstronne.

## 2. Decyzja

| Nr | Postanowienie |
|---|---|
| 1 | O kolejności decydują numery wersji nadawane przez serwer. Zegarom urządzeń się nie ufa |
| 2 | Konflikty rozwiązuje scalanie trójstronne, a wiersze, których nie da się scalić, zachowują obie wersje. Pierwszeństwo ma nieutracenie treści |
| 3 | CRDT nie zostaje przyjęty: notatki są krótkie, nie ma wymagania jednoczesnej edycji, a co najmniej dwukrotny wzrost rozmiaru treści nie jest tego wart |

## 3. Skutki

| Nr | Skutek |
|---|---|
| 1 | Urządzenie przechowuje `baseVersion` i dołącza go przy każdym wysłaniu |
| 2 | Pokazywanie konfliktu (REQ-006) staje się wymaganą funkcją urządzenia |
| 3 | Serwer przechowuje historię z ostatnich 30 dni (na potrzeby kosza oraz jako podstawę scalania trójstronnego) |
