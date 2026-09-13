---
navigation:
  order: 40
---

# 3.4 Ristiriitojen ratkaiseminen

| Tapaus | Sääntö |
|---|---|
| Samaa riviä muutettiin erikseen | Molemmat muutokset säilytetään: myöhemmin saapunut lisätään loppuun `>>>`-merkinnällä erotettuna. Käyttäjälle näytetään ristiriita (REQ-006) |
| Eri rivejä muutettiin | Yhdistetään automaattisesti kolmisuuntaisella yhdistämisellä; käyttäjälle ei ilmoiteta |
| Toinen puoli poisti | Poisto voittaa, ja toisen puolen sisältö siirtyy roskakoriin (REQ-005) |

Missään tapauksessa sisältöä ei menetetä (REQ-004).
