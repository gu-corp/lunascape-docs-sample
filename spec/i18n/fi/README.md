# Orbit-muistiinpanojen synkronointipalvelu — toiminnallinen määrittely

| Kohta | Sisältö |
|---|---|
| Dokumenttitunnus | ORB-SPEC-001 |
| Versio | 1.3 |
| Päivitetty | 2026-09-06 |
| Tila | Hyväksytty |
| Dokumentin vastuuhenkilö | Orbit-kehitystiimi (kuvitteellinen) |
| Liittyvät | ORB-REQ-001 (vaatimusluettelo), ORB-ADR-0001 (synkronointitavan valinta) |

## Muutoshistoria

| Versio | Päivämäärä | Muutoksen sisältö | Muuttaja |
|---|---|---|---|
| 1.0 | 2026-07-01 | Ensimmäinen versio | Orbit-kehitystiimi |
| 1.1 | 2026-08-10 | Lisätty ristiriitojen ratkaisusäännöt (3.4) | Orbit-kehitystiimi |
| 1.2 | 2026-09-06 | Lisätty API:n virhetaulukko (4.3) | Orbit-kehitystiimi |
| 1.3 | 2026-09-06 | Muutettu lukukohtaiseksi kansiorakenteeksi | Orbit-kehitystiimi |

## Rakenne

1. [Yleiskuvaus](01-overview/README.md) — tarkoitus, [rajaus ja oletukset](01-overview/scope.md), [termit](01-overview/terms.md)
2. [Vaatimukset](02-requirements/README.md) — [toiminnalliset vaatimukset](02-requirements/functional.md), [ei-toiminnalliset vaatimukset](02-requirements/non-functional.md), [vaatimusten jäljitettävyys](02-requirements/traceability.md)
3. [Rakenne](03-architecture/README.md) — [osat](03-architecture/components.md), [synkronoinnin kulku](03-architecture/sync-flow.md), [versionumerot](03-architecture/versioning.md), [ristiriitojen ratkaisu](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [päätepisteet](04-api/endpoints.md), [pyyntö ja vastaus](04-api/push.md), [virheet](04-api/errors.md)
5. [Suunnitteluratkaisut](05-decisions/README.md) — [ORB-ADR-0001 synkronointitavan valinta](05-decisions/0001-sync-method.md)

> **Tietoja tästä dokumentista**
> Tämä on kuvitteellinen määrittely, joka on laadittu esimerkiksi Lunascape Docsin kirjoitustavasta. Tuotetta tai yritystä ei ole olemassa. Se näyttää, miten lukukohtaisia kansioita, taulukoita, kaavioita (Mermaid), koodia ja käännöksiä käytetään.
