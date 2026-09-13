---
navigation:
  order: 30
---

# 3.3 Versionsnummer

Versionsnumret är ett monotont växande heltal som servern tilldelar per anteckning. Enheten skickar den senast mottagna versionen som `baseVersion`. När serverns aktuella version inte stämmer överens med `baseVersion` föreligger en konflikt (REQ-003). Enheternas klockor används inte för att bestämma ordningen ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
