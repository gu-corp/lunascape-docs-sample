---
navigation:
  order: 30
---

# 3. Architektura

Synchronizacja składa się z czterech elementów: klienta, API synchronizacji, magazynu i powiadomień ([elementy składowe](components.md)). [Przebieg synchronizacji](sync-flow.md) pokazuje kolejność, w jakiej zmiana trafia z urządzenia na serwer, a z serwera na pozostałe urządzenia. Podstawą tej kolejności są [numery wersji](versioning.md), a sposób postępowania, gdy dwie aktualizacje dotyczą tej samej wersji, określa [rozwiązywanie konfliktów](conflicts.md).
