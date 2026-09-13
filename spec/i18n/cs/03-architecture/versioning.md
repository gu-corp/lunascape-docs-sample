---
navigation:
  order: 30
---

# 3.3 Čísla verzí

Číslo verze je monotónně rostoucí celé číslo, které server přiděluje pro každou poznámku. Zařízení odesílá poslední přijatou verzi jako `baseVersion`. Pokud se aktuální verze na serveru neshoduje s `baseVersion`, jde o konflikt (REQ-003). Hodiny zařízení se pro určení pořadí nepoužívají ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
