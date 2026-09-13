---
navigation:
  order: 10
---

# ORB-ADR-0001 : retenir « versions attribuées par le serveur et fusion à trois voies » comme méthode de synchronisation

| Élément | Contenu |
|---|---|
| ID du document | ORB-ADR-0001 |
| Version | 1.0 |
| Date de mise à jour | 2026-07-01 |
| État | Approuvé |

## 1. Contexte

Les notes modifiées hors ligne sur plusieurs appareils doivent converger. Trois options étaient envisagées : (a) la dernière modification l'emporte selon l'horodatage, (b) un CRDT, (c) des numéros de version attribués par le serveur avec une fusion à trois voies.

## 2. Décision

| N° | Décision |
|---|---|
| 1 | L'ordre est déterminé par les numéros de version attribués par le serveur. L'horloge des appareils n'est pas considérée comme fiable |
| 2 | Les conflits sont résolus par une fusion à trois voies ; une ligne qui ne peut pas être fusionnée conserve les deux versions. Ne pas perdre de contenu est prioritaire |
| 3 | Le CRDT n'est pas retenu : les notes sont courtes, l'édition simultanée n'est pas requise, et doubler ou plus la taille du corps du texte ne justifie pas ce coût |

## 3. Conséquences

| N° | Conséquence |
|---|---|
| 1 | L'appareil conserve `baseVersion` et l'joint à chaque envoi |
| 2 | L'affichage des conflits (REQ-006) devient une fonction obligatoire de l'appareil |
| 3 | Le serveur conserve 30 jours d'historique (pour la corbeille et comme base des fusions à trois voies) |
