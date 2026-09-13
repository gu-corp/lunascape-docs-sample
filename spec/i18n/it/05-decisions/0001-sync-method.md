---
navigation:
  order: 10
---

# ORB-ADR-0001: adottare come metodo di sincronizzazione «versioni assegnate dal server e merge a tre vie»

| Voce | Contenuto |
|---|---|
| ID documento | ORB-ADR-0001 |
| Versione | 1.0 |
| Data di aggiornamento | 2026-07-01 |
| Stato | Approvato |

## 1. Contesto

Le note modificate offline su più dispositivi devono convergere. I candidati erano tre: (a) prevale l'ultima modifica in base all'orario, (b) un CRDT, (c) numeri di versione assegnati dal server con merge a tre vie.

## 2. Decisione

| N. | Decisione |
|---|---|
| 1 | L'ordine è stabilito dai numeri di versione assegnati dal server; l'orologio del dispositivo non è considerato attendibile |
| 2 | I conflitti si risolvono con un merge a tre vie; le righe che non è possibile risolvere conservano entrambe le versioni. La priorità è non perdere contenuti |
| 3 | Il CRDT non viene adottato: le note sono brevi, non c'è richiesta di modifica simultanea e il costo di raddoppiare o più la dimensione del testo non è giustificato |

## 3. Conseguenze

| N. | Conseguenza |
|---|---|
| 1 | Il dispositivo conserva `baseVersion` e lo allega a ogni invio |
| 2 | La visualizzazione dei conflitti (REQ-006) diventa una funzione obbligatoria del dispositivo |
| 3 | Il server conserva la cronologia degli ultimi 30 giorni (per il cestino e come base dei merge a tre vie) |
