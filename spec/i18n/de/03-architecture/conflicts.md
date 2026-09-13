---
navigation:
  order: 40
---

# 3.4 Konfliktlösung

| Fall | Regel |
|---|---|
| Dieselbe Zeile wurde unabhängig voneinander geändert | Beide Änderungen bleiben erhalten: die später eingetroffene wird, durch `>>>` abgetrennt, am Ende angefügt. Das Gerät zeigt einen Konflikt an (REQ-006) |
| Verschiedene Zeilen wurden geändert | Werden durch eine Drei-Wege-Zusammenführung automatisch zusammengeführt; der Benutzer wird nicht benachrichtigt |
| Eine Seite hat gelöscht | Die Löschung hat Vorrang, der Inhalt der anderen Seite wandert in den Papierkorb (REQ-005) |

In keinem Fall gehen Inhalte verloren (REQ-004).
