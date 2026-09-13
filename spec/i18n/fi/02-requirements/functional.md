---
navigation:
  order: 10
---

# 2.1 Toiminnalliset vaatimukset

| Tunnus | Vaatimus | Prioriteetti | Todennustapa |
|---|---|---|---|
| REQ-001 | Yhdellä laitteella luotu muistiinpano saavuttaa muut laitteet 10 sekunnin kuluessa yhteyden muodostamisesta | Pakollinen | Integraatiotesti |
| REQ-002 | Yhteydettömässä tilassa muokattu muistiinpano lähetetään automaattisesti, kun yhteys palaa | Pakollinen | Integraatiotesti |
| REQ-003 | Kaksi saman version päivitystä havaitaan ristiriidaksi | Pakollinen | Yksikkötesti |
| REQ-004 | Ristiriita ratkaistaan automaattisesti [kohdan 3.4 sääntöjen](../03-architecture/conflicts.md) mukaan menettämättä kummankaan puolen sisältöä | Pakollinen | Yksikkötesti |
| REQ-005 | Poisto välittyy muille laitteille, ja poistetun voi palauttaa roskakorista 30 päivän ajan | Suositeltava | Integraatiotesti |
| REQ-006 | Laite voi näyttää synkronoinnin tilan (synkronoitu, lähetetään, ristiriita) | Suositeltava | Silmämääräinen tarkistus |
