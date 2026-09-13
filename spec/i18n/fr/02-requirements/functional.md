---
navigation:
  order: 10
---

# 2.1 Exigences fonctionnelles

| ID | Exigence | Priorité | Méthode de vérification |
|---|---|---|---|
| REQ-001 | Une note créée sur un appareil parvient aux autres appareils dans les 10 secondes suivant la connexion | Obligatoire | Test d'intégration |
| REQ-002 | Une note modifiée hors ligne est envoyée automatiquement à la reconnexion | Obligatoire | Test d'intégration |
| REQ-003 | Deux mises à jour portant sur la même version sont détectées comme un conflit | Obligatoire | Test unitaire |
| REQ-004 | Un conflit est résolu automatiquement selon [les règles de la section 3.4](../03-architecture/conflicts.md), sans perdre le contenu de l'une ou l'autre partie | Obligatoire | Test unitaire |
| REQ-005 | Une suppression est répercutée sur les autres appareils et peut être restaurée depuis la corbeille pendant 30 jours | Recommandé | Test d'intégration |
| REQ-006 | Un appareil peut afficher l'état de la synchronisation (synchronisé, envoi en cours, conflit) | Recommandé | Contrôle visuel |
