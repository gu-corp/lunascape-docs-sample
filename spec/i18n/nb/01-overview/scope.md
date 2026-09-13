---
navigation:
  order: 20
---

# 1.2 Omfang og forutsetninger

## Omfang

| Nr. | Innenfor omfanget | Utenfor omfanget |
|---|---|---|
| 1 | Synkronisering av oppretting, oppdatering og sletting av notater | Samskriving av notater (deling av markør ved samtidig redigering) |
| 2 | Oppdaging og løsing av konflikter mellom enheter | Editoren på enheten |
| 3 | Synkroniserings-API-et (HTTP) | Betaling og kontoadministrasjon |

## Forutsetninger

- Enhetene er bare tilkoblet med jevne mellomrom. Redigering uten nett er utgangspunktet.
- Brødteksten i et notat er på høyst 1 MB.
- Rekkefølgen avhenger ikke av klokken på enheten; versjonsnumrene på serveren bestemmer den.
