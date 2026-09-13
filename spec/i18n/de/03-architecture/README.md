---
navigation:
  order: 30
---

# 3. Aufbau

Die Synchronisierung besteht aus vier Elementen: dem Client, der Synchronisierungs-API, dem Speicher und den Benachrichtigungen ([Bestandteile](components.md)). [Der Ablauf der Synchronisierung](sync-flow.md) zeigt, in welcher Reihenfolge eine Änderung vom Gerät zum Server und vom Server zu den anderen Geräten gelangt. Diese Reihenfolge beruht auf den [Versionsnummern](versioning.md); wie zwei Aktualisierungen behandelt werden, die auf derselben Version eintreffen, legt die [Konfliktlösung](conflicts.md) fest.
