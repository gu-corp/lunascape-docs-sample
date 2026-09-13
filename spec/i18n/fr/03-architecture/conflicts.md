---
navigation:
  order: 40
---

# 3.4 Résolution des conflits

| Cas | Règle |
|---|---|
| La même ligne a été modifiée séparément | Les deux modifications sont conservées : celle qui est arrivée en dernier est ajoutée à la fin, précédée du séparateur `>>>`. Un conflit est signalé à l'utilisateur (REQ-006) |
| Des lignes différentes ont été modifiées | La fusion à trois voies intègre les modifications automatiquement ; l'utilisateur n'en est pas informé |
| L'une des parties a supprimé | La suppression l'emporte et le contenu de l'autre partie est placé dans la corbeille (REQ-005) |

Dans tous les cas, aucun contenu n'est perdu (REQ-004).
