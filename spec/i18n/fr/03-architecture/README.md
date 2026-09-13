---
navigation:
  order: 30
---

# 3. Architecture

La synchronisation repose sur quatre éléments : le client, l'API de synchronisation, le magasin et les notifications ([composants](components.md)). [Le flux de synchronisation](sync-flow.md) indique l'ordre dans lequel une modification parvient de l'appareil au serveur, puis du serveur aux autres appareils. Cet ordre se fonde sur les [numéros de version](versioning.md) ; le traitement de deux mises à jour portant sur la même version est défini dans [la résolution des conflits](conflicts.md).
