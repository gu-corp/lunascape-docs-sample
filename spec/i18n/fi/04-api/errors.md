---
navigation:
  order: 30
---

# 4.3 Virheet

| Tila | Merkitys | Laitteen toimenpide |
|---|---|---|
| 400 | Pyynnön muoto on virheellinen | Lopeta lähettäminen ja kirjaa lokiin |
| 401 | Token on virheellinen | Tunnistaudu uudelleen |
| 409 | Versiot eivät täsmää (ristiriita) | Korvaa vastauksen `body`-sisällöllä ja näytä ristiriita |
| 413 | Runko ylittää 1 Mt | Ilmoita käyttäjälle äläkä lähetä |
| 429 | Pyyntöjä on liikaa | Odota `Retry-After`-kentän ilmoittamat sekunnit ja lähetä uudelleen |
| 5xx | Palvelinvirhe | Lähetä uudelleen eksponentiaalisella viiveellä (enintään 5 kertaa) |
