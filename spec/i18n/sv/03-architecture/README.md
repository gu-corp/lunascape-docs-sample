---
navigation:
  order: 30
---

# 3. Arkitektur

Synkroniseringen består av fyra delar: klienten, synkroniserings-API:et, lagret och aviseringarna ([komponenter](components.md)). [Synkroniseringsflödet](sync-flow.md) visar i vilken ordning en ändring når servern från en enhet och andra enheter från servern. Ordningen vilar på [versionsnummer](versioning.md); hur två uppdateringar som träffar samma version hanteras anges i [konfliktlösning](conflicts.md).
