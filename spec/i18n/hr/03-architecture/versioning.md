---
navigation:
  order: 30
---

# 3.3 Brojevi verzija

Broj verzije je monotono rastući cijeli broj koji poslužitelj dodjeljuje svakoj bilješci. Uređaj šalje posljednju verziju koju je primio kao `baseVersion`. Kada se trenutačna verzija na poslužitelju ne podudara s `baseVersion`, radi se o sukobu (REQ-003). Satovi uređaja ne sudjeluju u određivanju redoslijeda ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
