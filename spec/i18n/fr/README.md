# Service de synchronisation de notes Orbit — Spécification fonctionnelle

| Élément | Contenu |
|---|---|
| ID du document | ORB-SPEC-001 |
| Version | 1.3 |
| Date de mise à jour | 2026-09-06 |
| État | Approuvé |
| Responsable du document | Équipe de développement Orbit (fictive) |
| Documents liés | ORB-REQ-001 (liste des exigences), ORB-ADR-0001 (choix du mode de synchronisation) |

## Historique des révisions

| Version | Date | Contenu de la révision | Auteur |
|---|---|---|---|
| 1.0 | 2026-07-01 | Version initiale | Équipe de développement Orbit |
| 1.1 | 2026-08-10 | Ajout des règles de résolution des conflits (3.4) | Équipe de développement Orbit |
| 1.2 | 2026-09-06 | Ajout du tableau des erreurs de l'API (4.3) | Équipe de développement Orbit |
| 1.3 | 2026-09-06 | Réorganisation en un dossier par chapitre | Équipe de développement Orbit |

## Structure

1. [Présentation](01-overview/README.md) — objet, [périmètre et hypothèses](01-overview/scope.md), [terminologie](01-overview/terms.md)
2. [Exigences](02-requirements/README.md) — [exigences fonctionnelles](02-requirements/functional.md), [exigences non fonctionnelles](02-requirements/non-functional.md), [suivi des exigences](02-requirements/traceability.md)
3. [Architecture](03-architecture/README.md) — [composants](03-architecture/components.md), [déroulement de la synchronisation](03-architecture/sync-flow.md), [numéros de version](03-architecture/versioning.md), [résolution des conflits](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [points de terminaison](04-api/endpoints.md), [requête et réponse](04-api/push.md), [erreurs](04-api/errors.md)
5. [Décisions de conception](05-decisions/README.md) — [ORB-ADR-0001, choix du mode de synchronisation](05-decisions/0001-sync-method.md)

> **À propos de ce document**
> Il s'agit d'une spécification fictive rédigée comme exemple de ce que l'on peut écrire avec Lunascape Docs. Ni le produit ni l'entreprise n'existent réellement. Elle montre l'usage d'un dossier par chapitre, des tableaux, des schémas (Mermaid), du code et des traductions.
