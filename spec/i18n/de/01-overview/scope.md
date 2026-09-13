---
navigation:
  order: 20
---

# 1.2 Umfang und Voraussetzungen

## Umfang

| Nr. | Im Umfang enthalten | Nicht im Umfang enthalten |
|---|---|---|
| 1 | Synchronisierung von Erstellung, Aktualisierung und Löschung von Notizen | Gemeinsames Bearbeiten von Notizen (geteilte Cursor beim gleichzeitigen Bearbeiten) |
| 2 | Erkennen und Auflösen von Konflikten zwischen Geräten | Der Editor auf dem Gerät |
| 3 | Die Synchronisierungs-API (HTTP) | Abrechnung, Kontoverwaltung |

## Voraussetzungen

- Geräte sind nur zeitweise verbunden. Das Bearbeiten im Offlinebetrieb wird vorausgesetzt.
- Der Text einer Notiz ist auf 1 MB begrenzt.
- Die Reihenfolge hängt nicht von der Uhr des Geräts ab, sondern wird durch die Versionsnummern des Servers bestimmt.
