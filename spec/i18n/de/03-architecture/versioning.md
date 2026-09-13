---
navigation:
  order: 30
---

# 3.3 Versionsnummern

Die Versionsnummer ist eine monoton steigende ganze Zahl, die der Server je Notiz vergibt. Das Gerät sendet die zuletzt empfangene Version als `baseVersion`. Stimmt die aktuelle Version des Servers nicht mit `baseVersion` überein, liegt ein Konflikt vor (REQ-003). Die Uhr des Geräts wird für die Festlegung der Reihenfolge nicht herangezogen ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
