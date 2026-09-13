---
navigation:
  order: 20
---

# 1.2 Reikwijdte en aannames

## Reikwijdte

| Nr. | Binnen de reikwijdte | Buiten de reikwijdte |
|---|---|---|
| 1 | Het synchroniseren van het aanmaken, bijwerken en verwijderen van notities | Het samen bewerken van notities (gedeelde cursors bij gelijktijdig bewerken) |
| 2 | Het opsporen en oplossen van conflicten tussen apparaten | De editor op het apparaat |
| 3 | De synchronisatie-API (HTTP) | Facturering, accountbeheer |

## Aannames

- Apparaten hebben slechts met tussenpozen verbinding. Offline bewerken is het uitgangspunt.
- De tekst van een notitie is ten hoogste 1 MB.
- De vololgorde hangt niet af van de klok van het apparaat; de versienummers van de server bepalen de volgorde.
