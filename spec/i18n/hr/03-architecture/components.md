---
navigation:
  order: 10
---

# 3.1 Sastavni dijelovi

| Element | Uloga |
|---|---|
| Klijent | Prati uređivanje bilježaka, stavlja promjene u red čekanja i šalje ih poslužitelju pri povezivanju |
| API za sinkronizaciju | Prima promjene, dodjeljuje brojeve verzija i raspodjeljuje ih ostalim uređajima |
| Spremište | Trenutačni sadržaj svake bilješke i povijest zadnjih 30 dana |
| Obavijesti | Uređaju na kojem je došlo do promjene šalje lagani signal koji potiče dohvaćanje |

```mermaid
flowchart TB
  subgraph A[Uređaj A]
    EA[Uređivač] --> QA[Red čekanja]
  end
  subgraph B[Uređaj B]
    EB[Uređivač] --> QB[Red čekanja]
  end
  QA -- push --> API[API za sinkronizaciju]
  QB -- push --> API
  API --> STORE[(Spremište)]
  API --> NOTIFY[Obavijesti]
  NOTIFY -. potiče pull .-> QA
  NOTIFY -. potiče pull .-> QB
```
