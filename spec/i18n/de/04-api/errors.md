---
navigation:
  order: 30
---

# 4.3 Fehler

| Status | Bedeutung | Verhalten des Geräts |
|---|---|---|
| 400 | Fehlerhaft aufgebaute Anfrage | Senden einstellen und protokollieren |
| 401 | Token ungültig | Erneut authentifizieren |
| 409 | Versionskonflikt | Durch `body` der Antwort ersetzen und Konflikt anzeigen |
| 413 | Rumpf größer als 1 MB | Benutzer benachrichtigen und nicht senden |
| 429 | Zu viele Anfragen | Die in `Retry-After` genannten Sekunden warten, dann erneut senden |
| 5xx | Serverfehler | Mit exponentiellem Backoff erneut senden (höchstens 5-mal) |
