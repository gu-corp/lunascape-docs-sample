---
navigation:
  order: 10
---

# ORB-ADR-0001: „Serverseitig vergebene Versionen mit Drei-Wege-Merge" als Synchronisationsverfahren festlegen

| Punkt | Inhalt |
|---|---|
| Dokument-ID | ORB-ADR-0001 |
| Version | 1.0 |
| Aktualisiert am | 2026-07-01 |
| Status | Genehmigt |

## 1. Hintergrund

Notizen, die offline auf mehreren Geräten bearbeitet werden, müssen zusammengeführt werden. Es standen drei Kandidaten zur Auswahl: (a) der letzte Änderungszeitpunkt gewinnt, (b) ein CRDT, (c) serverseitig vergebene Versionsnummern mit einem Drei-Wege-Merge.

## 2. Entscheidung

| Nr. | Entscheidung |
|---|---|
| 1 | Die Reihenfolge wird durch die vom Server vergebenen Versionsnummern bestimmt. Den Uhren der Geräte wird nicht vertraut |
| 2 | Konflikte werden durch einen Drei-Wege-Merge aufgelöst; bei einer Zeile, die sich nicht auflösen lässt, bleiben beide Seiten erhalten. Vorrang hat, keine Inhalte zu verlieren |
| 3 | Ein CRDT wird nicht eingesetzt: Die Notizen sind kurz, gleichzeitiges Bearbeiten wird nicht verlangt, und der Preis einer mindestens doppelt so großen Textmenge steht dazu in keinem Verhältnis |

## 3. Auswirkungen

| Nr. | Auswirkung |
|---|---|
| 1 | Ein Gerät hält `baseVersion` vor und legt sie jeder Übertragung bei |
| 2 | Die Anzeige eines Konflikts (REQ-006) wird zur Pflichtfunktion des Geräts |
| 3 | Der Server bewahrt die Historie der letzten 30 Tage auf (für den Papierkorb und als Basis für Drei-Wege-Merges) |
