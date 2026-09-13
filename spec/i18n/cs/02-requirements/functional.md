---
navigation:
  order: 10
---

# 2.1 Funkční požadavky

| ID | Požadavek | Priorita | Způsob ověření |
|---|---|---|---|
| REQ-001 | Poznámka vytvořená na jednom zařízení se do 10 sekund po připojení dostane na ostatní zařízení | Povinné | Integrační test |
| REQ-002 | Poznámka upravená offline se při opětovném připojení odešle automaticky | Povinné | Integrační test |
| REQ-003 | Dvě úpravy téže verze jsou rozpoznány jako konflikt | Povinné | Jednotkový test |
| REQ-004 | Konflikt se automaticky vyřeší podle [pravidel v 3.4](../03-architecture/conflicts.md), aniž by se ztratil obsah kterékoli strany | Povinné | Jednotkový test |
| REQ-005 | Smazání se promítne i na ostatní zařízení a po dobu 30 dnů jej lze obnovit z koše | Doporučené | Integrační test |
| REQ-006 | Zařízení umí zobrazit stav synchronizace (synchronizováno, odesílá se, konflikt) | Doporučené | Vizuální kontrola |
