---
navigation:
  order: 30
---

# 3. Arkitektur

Synkronisering består af fire elementer: klienten, synkroniserings-API'et, lageret og notifikationer ([komponenter](components.md)). [Synkroniseringsforløbet](sync-flow.md) viser den rækkefølge, hvori en ændring når fra en enhed til serveren og fra serveren videre til andre enheder. Rækkefølgen bygger på [versionsnumre](versioning.md), og hvordan to opdateringer til samme version håndteres, er fastlagt i [konfliktløsning](conflicts.md).
