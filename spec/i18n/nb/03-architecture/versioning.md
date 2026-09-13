---
navigation:
  order: 30
---

# 3.3 Versjonsnumre

Versjonsnummeret er et monotont økende heltall som serveren tildeler per notat. En enhet sender den siste versjonen den har mottatt, som `baseVersion`. Når serverens gjeldende versjon ikke stemmer overens med `baseVersion`, er det en konflikt (REQ-003). Enhetenes klokker brukes ikke til å avgjøre rekkefølgen ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
