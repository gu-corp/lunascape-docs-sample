---
navigation:
  order: 30
---

# 3.3 Numere de versiune

Numărul de versiune este un întreg monoton crescător pe care serverul îl atribuie fiecărei notițe. Dispozitivul trimite ultima versiune primită ca `baseVersion`. Când versiunea curentă a serverului nu corespunde cu `baseVersion`, avem un conflict (REQ-003). Ceasul dispozitivului nu este folosit pentru stabilirea ordinii ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
