---
navigation:
  order: 30
---

# 3.3 Numéros de version

Le numéro de version est un entier croissant de façon monotone que le serveur attribue à chaque note. Un appareil envoie la dernière version qu'il a reçue comme `baseVersion`. Lorsque la version courante du serveur ne correspond pas à `baseVersion`, il y a conflit (REQ-003). L'horloge des appareils n'intervient pas dans la détermination de l'ordre ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
