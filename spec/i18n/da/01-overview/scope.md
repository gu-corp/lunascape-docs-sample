---
navigation:
  order: 20
---

# 1.2 Omfang og forudsætninger

## Omfang

| Nr. | Med i omfanget | Uden for omfanget |
|---|---|---|
| 1 | Synkronisering af oprettelse, opdatering og sletning af noter | Fælles redigering af noter (delte markører ved samtidig redigering) |
| 2 | Registrering og løsning af konflikter mellem enheder | Editoren på enheden |
| 3 | Synkroniserings-API'et (HTTP) | Betaling og administration af konti |

## Forudsætninger

- Enhederne er kun forbundet med afbrydelser. Redigering offline er forudsat.
- En notes brødtekst er højst 1 MB.
- Rækkefølgen afhænger ikke af enhedens ur; serverens versionsnumre afgør den.
