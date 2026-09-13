---
navigation:
  order: 10
---

# ORB-ADR-0001: Synkronointitavaksi valitaan "palvelimen antamat versiot ja kolmisuuntainen yhdistäminen"

| Kohta | Sisältö |
|---|---|
| Dokumentin tunnus | ORB-ADR-0001 |
| Versio | 1.0 |
| Päivitetty | 2026-07-01 |
| Tila | Hyväksytty |

## 1. Tausta

Usealla laitteella offline-tilassa muokatut muistiinpanot on saatava yhtenemään. Vaihtoehtoja oli kolme: (a) viimeisin muokkausaika voittaa, (b) CRDT, (c) palvelimen antamat versionumerot ja kolmisuuntainen yhdistäminen.

## 2. Päätös

| Nro | Päätös |
|---|---|
| 1 | Järjestys määräytyy palvelimen antamien versionumeroiden mukaan. Laitteiden kelloihin ei luoteta |
| 2 | Ristiriidat ratkaistaan kolmisuuntaisella yhdistämisellä, ja rivit, joita ei voi ratkaista, säilytetään molempina. Etusijalla on se, ettei sisältöä menetetä |
| 3 | CRDT:tä ei oteta käyttöön. Muistiinpanot ovat lyhyitä, samanaikaiselle muokkaukselle ei ole tarvetta, eikä leipätekstin koon kaksinkertaistuminen tai enemmän ole hintansa arvoinen |

## 3. Vaikutukset

| Nro | Vaikutus |
|---|---|
| 1 | Laite säilyttää `baseVersion`-arvon ja liittää sen jokaiseen lähetykseen |
| 2 | Ristiriidan näyttämisestä (REQ-006) tulee laitteen pakollinen ominaisuus |
| 3 | Palvelin säilyttää viimeisten 30 päivän historian (roskakoria ja kolmisuuntaisen yhdistämisen perustaa varten) |
