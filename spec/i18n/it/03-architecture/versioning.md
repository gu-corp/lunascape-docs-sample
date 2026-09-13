---
navigation:
  order: 30
---

# 3.3 Numeri di versione

Il numero di versione è un intero monotonicamente crescente che il server assegna a ciascuna nota. Il dispositivo invia come `baseVersion` l'ultima versione ricevuta. Quando la versione corrente del server non coincide con `baseVersion`, si tratta di un conflitto (REQ-003). L'orologio del dispositivo non viene usato per determinare l'ordine ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
