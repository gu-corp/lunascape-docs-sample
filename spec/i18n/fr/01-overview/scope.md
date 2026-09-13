---
navigation:
  order: 20
---

# 1.2 Périmètre et hypothèses

## Périmètre

| N° | Dans le périmètre | Hors périmètre |
|---|---|---|
| 1 | Synchronisation de la création, de la mise à jour et de la suppression des notes | Édition collaborative des notes (partage du curseur en édition simultanée) |
| 2 | Détection et résolution des conflits entre appareils | L'éditeur présent sur l'appareil |
| 3 | L'API de synchronisation (HTTP) | La facturation, la gestion des comptes |

## Hypothèses

- Les appareils ne sont connectés que par intermittence. L'édition hors ligne est le cas normal.
- Le corps d'une note est limité à 1 Mo.
- L'ordre ne dépend pas de l'horloge des appareils : il est déterminé par les numéros de version du serveur.
