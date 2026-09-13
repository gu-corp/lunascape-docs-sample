---
navigation:
  order: 30
---

# 2.3 Vaatimusten jäljitettävyys

Vaatimukset kytketään [arkkitehtuurin](../03-architecture/README.md) osiin ja [API:n](../04-api/README.md) päätepisteisiin. Vaatimusta, jolla ei ole vastinetta, käsitellään toteuttamattomana.

```mermaid
flowchart LR
  REQ001[REQ-001 saapuu 10 sekunnissa] --> PUSH["/notes/push"]
  REQ002[REQ-002 lähetys yhteyden palattua] --> QUEUE[Laitteen puoleinen jono]
  REQ003[REQ-003 ristiriitojen havaitseminen] --> VERSION[Versionumeron tarkistus]
  REQ004[REQ-004 automaattinen ratkaisu] --> MERGE[Kolmisuuntainen yhdistäminen]
  QUEUE --> PUSH
  VERSION --> MERGE
```
