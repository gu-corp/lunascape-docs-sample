---
navigation:
  order: 30
---

# 3. Architectuur

Synchronisatie bestaat uit vier elementen: de client, de synchronisatie-API, de opslag en de meldingen ([bouwstenen](components.md)). [De synchronisatiestroom](sync-flow.md) laat zien in welke volgorde een wijziging van een apparaat naar de server gaat, en van de server naar andere apparaten. Die volgorde berust op [versienummers](versioning.md); hoe twee wijzigingen op dezelfde versie worden afgehandeld, is vastgelegd in [conflictoplossing](conflicts.md).
