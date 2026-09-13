---
navigation:
  order: 10
---

# 3.1 Osat

| Osa | Tehtävä |
|---|---|
| Asiakasohjelma | Tarkkailee muistiinpanojen muokkauksia, asettaa muutokset jonoon ja lähettää ne palvelimelle yhteyden muodostuessa |
| Synkronointirajapinta | Ottaa muutokset vastaan, numeroi versiot ja jakaa ne muihin laitteisiin |
| Tietovarasto | Säilyttää kunkin muistiinpanon nykyisen sisällön ja viimeisten 30 päivän historian |
| Ilmoitukset | Lähettää muutoksen tapahtuessa kevyen viestin, joka kehottaa laitetta noutamaan muutokset |

```mermaid
flowchart TB
  subgraph A[Laite A]
    EA[Editori] --> QA[Jono]
  end
  subgraph B[Laite B]
    EB[Editori] --> QB[Jono]
  end
  QA -- push --> API[Synkronointirajapinta]
  QB -- push --> API
  API --> STORE[(Tietovarasto)]
  API --> NOTIFY[Ilmoitukset]
  NOTIFY -. kehottaa noutamaan .-> QA
  NOTIFY -. kehottaa noutamaan .-> QB
```
