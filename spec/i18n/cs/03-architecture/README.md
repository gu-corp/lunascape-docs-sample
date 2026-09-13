---
navigation:
  order: 30
---

# 3. Architektura

Synchronizace se skládá ze čtyř prvků: klienta, synchronizačního API, úložiště dat a oznámení ([součásti](components.md)). [Průběh synchronizace](sync-flow.md) ukazuje pořadí, v jakém změna putuje ze zařízení na server a ze serveru k dalším zařízením. Toto pořadí se opírá o [čísla verzí](versioning.md); jak se zachází se dvěma aktualizacemi, které dorazí ke stejné verzi, určuje [řešení konfliktů](conflicts.md).
