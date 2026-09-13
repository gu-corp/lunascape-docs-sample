---
navigation:
  order: 30
---

# 3.3 Versienummers

Het versienummer is een monotoon oplopend geheel getal dat de server per notitie toekent. Een apparaat stuurt de laatst ontvangen versie mee als `baseVersion`. Komt de huidige versie op de server niet overeen met `baseVersion`, dan is dat een conflict (REQ-003). De klok van het apparaat speelt geen rol bij het bepalen van de volgorde ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
