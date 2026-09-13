---
navigation:
  order: 20
---

# 1.2 Ambito e presupposti

## Ambito

| N. | Incluso nell'ambito | Escluso dall'ambito |
|---|---|---|
| 1 | Sincronizzazione di creazione, aggiornamento ed eliminazione delle note | Modifica collaborativa delle note (cursori condivisi durante la modifica simultanea) |
| 2 | Rilevamento e risoluzione dei conflitti tra dispositivi | L'editor sul dispositivo |
| 3 | API di sincronizzazione (HTTP) | Fatturazione, gestione dell'account |

## Presupposti

- I dispositivi si connettono solo a intermittenza. Si presuppone la modifica offline.
- Il corpo di una nota ha un limite massimo di 1 MB.
- L'ordine non dipende dall'orologio del dispositivo: lo determinano i numeri di versione del server.
