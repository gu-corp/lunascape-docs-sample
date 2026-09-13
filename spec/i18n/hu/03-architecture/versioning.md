---
navigation:
  order: 30
---

# 3.3 Verziószámok

A verziószám monoton növekvő egész szám, amelyet a kiszolgáló jegyzetenként oszt ki. A készülék az utoljára kapott verziót küldi el `baseVersion` néven. Ha a kiszolgáló aktuális verziója nem egyezik a `baseVersion` értékkel, az ütközésnek számít (REQ-003). A készülékek órája nem játszik szerepet a sorrend meghatározásában ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
