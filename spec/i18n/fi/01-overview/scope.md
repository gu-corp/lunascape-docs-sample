---
navigation:
  order: 20
---

# 1.2 Laajuus ja oletukset

## Laajuus

| Nro | Kuuluu laajuuteen | Ei kuulu laajuuteen |
|---|---|---|
| 1 | Muistiinpanojen luonnin, päivityksen ja poiston synkronointi | Muistiinpanojen yhteismuokkaus (kohdistimien jakaminen samanaikaisessa muokkauksessa) |
| 2 | Laitteiden välisten ristiriitojen havaitseminen ja ratkaiseminen | Laitteen oma editori |
| 3 | Synkronointirajapinta (HTTP) | Laskutus ja tilien hallinta |

## Oletukset

- Laitteet ovat yhteydessä vain ajoittain. Muokkaaminen offline-tilassa on lähtökohta.
- Muistiinpanon leipätekstin yläraja on 1 Mt.
- Järjestys ei riipu laitteen kellosta, vaan sen ratkaisevat palvelimen versionumerot.
