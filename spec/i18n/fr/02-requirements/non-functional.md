---
navigation:
  order: 20
---

# 2.2 Exigences non fonctionnelles

| ID | Exigence | Objectif |
|---|---|---|
| NFR-001 | Temps de réponse de l'API de synchronisation | Moins de 300 ms au 95e centile |
| NFR-002 | Disponibilité | 99,9 % par mois |
| NFR-003 | Protection des échanges | TLS 1.3. Le corps des notes est chiffré lors de son stockage sur le serveur |
| NFR-004 | Nombre de notes par utilisateur | Les exigences de performance sont tenues jusqu'à 100 000 notes |
