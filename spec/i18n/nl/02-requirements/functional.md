---
navigation:
  order: 10
---

# 2.1 Functionele eisen

| ID | Eis | Prioriteit | Verificatiemethode |
|---|---|---|---|
| REQ-001 | Een notitie die op een apparaat is gemaakt, bereikt binnen 10 seconden na verbinding de andere apparaten | Verplicht | Integratietest |
| REQ-002 | Een offline bewerkte notitie wordt bij het herstellen van de verbinding automatisch verzonden | Verplicht | Integratietest |
| REQ-003 | Twee wijzigingen op dezelfde versie worden als conflict gedetecteerd | Verplicht | Unittest |
| REQ-004 | Een conflict wordt automatisch opgelost volgens [de regels in 3.4](../03-architecture/conflicts.md), zonder dat de inhoud van een van beide verloren gaat | Verplicht | Unittest |
| REQ-005 | Een verwijdering wordt ook op de andere apparaten doorgevoerd en kan 30 dagen lang uit de Prullenbak worden hersteld | Aanbevolen | Integratietest |
| REQ-006 | Een apparaat kan de synchronisatiestatus tonen (gesynchroniseerd, bezig met verzenden, conflict) | Aanbevolen | Visuele inspectie |
