---
navigation:
  order: 30
---

# 3. Arkitektur

Synkronisering består av fire elementer: klienten, synkroniserings-API-et, lageret og varslene ([komponenter](components.md)). [Synkroniseringsflyten](sync-flow.md) viser rekkefølgen en endring går i fra en enhet til serveren, og fra serveren til andre enheter. Rekkefølgen bygger på [versjonsnumre](versioning.md); hvordan to oppdateringer mot samme versjon håndteres, er fastsatt i [konfliktløsning](conflicts.md).
