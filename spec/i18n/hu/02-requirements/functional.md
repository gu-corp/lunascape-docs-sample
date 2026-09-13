---
navigation:
  order: 10
---

# 2.1 Funkcionális követelmények

| Azonosító | Követelmény | Prioritás | Ellenőrzés módja |
|---|---|---|---|
| REQ-001 | Az egyik eszközön létrehozott jegyzet a csatlakozás után 10 másodpercen belül eljut a többi eszközre | Kötelező | Integrációs teszt |
| REQ-002 | Az offline szerkesztett jegyzet az újracsatlakozáskor automatikusan elküldésre kerül | Kötelező | Integrációs teszt |
| REQ-003 | Ugyanazon változat két frissítése ütközésként kerül felismerésre | Kötelező | Egységteszt |
| REQ-004 | Az ütközést [a 3.4 szabályai](../03-architecture/conflicts.md) automatikusan feloldják, egyik fél tartalmának elvesztése nélkül | Kötelező | Egységteszt |
| REQ-005 | A törlés a többi eszközre is érvényesül, és 30 napig visszaállítható a Kukából | Ajánlott | Integrációs teszt |
| REQ-006 | Az eszköz meg tudja jeleníteni a szinkronizálás állapotát (szinkronizálva, küldés alatt, ütközés) | Ajánlott | Szemrevételezés |
