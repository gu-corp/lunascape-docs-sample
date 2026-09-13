---
navigation:
  order: 30
---

# 3.3 Versionsnumre

Versionsnummeret er et monotont voksende heltal, som serveren tildeler pr. note. En enhed sender den senest modtagne version som `baseVersion`. Når serverens aktuelle version ikke stemmer overens med `baseVersion`, er det en konflikt (REQ-003). Enhedernes ure indgår ikke i fastlæggelsen af rækkefølgen ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
