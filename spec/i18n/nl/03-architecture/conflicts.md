---
navigation:
  order: 40
---

# 3.4 Conflictoplossing

| Geval | Regel |
|---|---|
| Dezelfde regel is afzonderlijk gewijzigd | Beide wijzigingen blijven behouden: de wijziging die later binnenkomt, wordt met `>>>` gescheiden aan het einde toegevoegd. De gebruiker krijgt te zien dat er een conflict is (REQ-006) |
| Verschillende regels zijn gewijzigd | Deze worden automatisch samengevoegd met een driewegsamenvoeging. De gebruiker krijgt hiervan geen melding |
| Eén kant heeft verwijderd | De verwijdering krijgt voorrang; de inhoud van de andere kant gaat naar de Prullenbak (REQ-005) |

In alle gevallen gaat er geen inhoud verloren (REQ-004).
