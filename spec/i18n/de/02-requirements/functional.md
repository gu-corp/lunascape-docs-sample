---
navigation:
  order: 10
---

# 2.1 Funktionale Anforderungen

| ID | Anforderung | Priorität | Prüfverfahren |
|---|---|---|---|
| REQ-001 | Eine auf einem Gerät erstellte Notiz erreicht die anderen Geräte innerhalb von 10 Sekunden nach dem Verbinden | Erforderlich | Integrationstest |
| REQ-002 | Eine offline bearbeitete Notiz wird beim erneuten Verbinden automatisch gesendet | Erforderlich | Integrationstest |
| REQ-003 | Zwei Aktualisierungen derselben Version werden als Konflikt erkannt | Erforderlich | Modultest |
| REQ-004 | Ein Konflikt wird nach [den Regeln in 3.4](../03-architecture/conflicts.md) automatisch aufgelöst, ohne den Inhalt einer der beiden Seiten zu verlieren | Erforderlich | Modultest |
| REQ-005 | Eine Löschung wird auf die anderen Geräte übertragen und lässt sich 30 Tage lang aus dem Papierkorb wiederherstellen | Empfohlen | Integrationstest |
| REQ-006 | Ein Gerät kann den Synchronisationsstatus anzeigen (synchronisiert, wird gesendet, Konflikt) | Empfohlen | Sichtprüfung |
