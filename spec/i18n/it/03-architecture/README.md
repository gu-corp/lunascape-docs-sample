---
navigation:
  order: 30
---

# 3. Architettura

La sincronizzazione si compone di quattro elementi: il client, l'API di sincronizzazione, l'archivio e le notifiche ([componenti](components.md)). [Il flusso di sincronizzazione](sync-flow.md) mostra l'ordine in cui una modifica viaggia dal dispositivo al server e dal server agli altri dispositivi. Tale ordine si fonda sui [numeri di versione](versioning.md); il trattamento di due aggiornamenti che ricadono sulla stessa versione è definito in [risoluzione dei conflitti](conflicts.md).
