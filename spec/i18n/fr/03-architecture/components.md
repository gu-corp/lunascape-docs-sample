---
navigation:
  order: 10
---

# 3.1 Composants

| Élément | Rôle |
|---|---|
| Client | Surveille les modifications des notes, met les changements en file d'attente et les envoie au serveur lors de la connexion |
| API de synchronisation | Accepte les changements, attribue les numéros de version et les distribue aux autres appareils |
| Magasin | Contenu actuel de chaque note et historique des 30 derniers jours |
| Notifications | Envoie un signal léger à l'appareil concerné pour l'inviter à récupérer les changements |

```mermaid
flowchart TB
  subgraph A[Appareil A]
    EA[Éditeur] --> QA[File d'attente]
  end
  subgraph B[Appareil B]
    EB[Éditeur] --> QB[File d'attente]
  end
  QA -- push --> API[API de synchronisation]
  QB -- push --> API
  API --> STORE[(Magasin)]
  API --> NOTIFY[Notifications]
  NOTIFY -. invite à un pull .-> QA
  NOTIFY -. invite à un pull .-> QB
```
