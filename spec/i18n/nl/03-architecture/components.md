---
navigation:
  order: 10
---

# 3.1 Onderdelen

| Element | Rol |
|---|---|
| Client | Bewaakt bewerkingen van notities, plaatst de wijzigingen in een wachtrij en stuurt ze bij verbinding naar de server |
| Synchronisatie-API | Neemt wijzigingen aan, kent versienummers toe en verspreidt ze naar andere apparaten |
| Opslag | Bevat de huidige inhoud van elke notitie en de geschiedenis van de afgelopen 30 dagen |
| Meldingen | Stuurt een licht signaal naar een apparaat om op te halen wanneer er een wijziging is |

```mermaid
flowchart TB
  subgraph A[Apparaat A]
    EA[Editor] --> QA[Wachtrij]
  end
  subgraph B[Apparaat B]
    EB[Editor] --> QB[Wachtrij]
  end
  QA -- push --> API[Synchronisatie-API]
  QB -- push --> API
  API --> STORE[(Opslag)]
  API --> NOTIFY[Meldingen]
  NOTIFY -. spoort aan tot pull .-> QA
  NOTIFY -. spoort aan tot pull .-> QB
```
