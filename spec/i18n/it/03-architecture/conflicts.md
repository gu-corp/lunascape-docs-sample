---
navigation:
  order: 40
---

# 3.4 Risoluzione dei conflitti

| Caso | Regola |
|---|---|
| La stessa riga è stata modificata separatamente | Si conservano entrambe le modifiche: quella arrivata dopo viene aggiunta in fondo, separata da `>>>`. All'utente viene segnalato un conflitto (REQ-006) |
| Sono state modificate righe diverse | Le modifiche vengono unite automaticamente con una fusione a tre vie; l'utente non viene avvisato |
| Una delle due parti ha eliminato la nota | L'eliminazione ha la precedenza e il contenuto dell'altra parte finisce nel cestino (REQ-005) |

In ogni caso non si perde alcun contenuto (REQ-004).
