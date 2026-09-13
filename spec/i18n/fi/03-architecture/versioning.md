---
navigation:
  order: 30
---

# 3.3 Versionumerot

Versionumero on monotonisesti kasvava kokonaisluku, jonka palvelin määrittää muistiinpanokohtaisesti. Laite lähettää viimeksi saamansa version arvona `baseVersion`. Kun palvelimen nykyinen versio ei vastaa arvoa `baseVersion`, kyseessä on ristiriita (REQ-003). Laitteiden kelloja ei käytetä järjestyksen määrittämiseen ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
