---
navigation:
  order: 10
---

# 2.1 Requisiti funzionali

| ID | Requisito | Priorità | Metodo di verifica |
|---|---|---|---|
| REQ-001 | Una nota creata su un dispositivo raggiunge gli altri dispositivi entro 10 secondi dalla connessione | Obbligatorio | Test di integrazione |
| REQ-002 | Una nota modificata offline viene inviata automaticamente alla riconnessione | Obbligatorio | Test di integrazione |
| REQ-003 | Due aggiornamenti sulla stessa versione vengono rilevati come conflitto | Obbligatorio | Test unitario |
| REQ-004 | Il conflitto viene risolto automaticamente secondo [le regole del punto 3.4](../03-architecture/conflicts.md), senza perdere il contenuto di nessuna delle due parti | Obbligatorio | Test unitario |
| REQ-005 | L'eliminazione viene propagata agli altri dispositivi ed è ripristinabile dal cestino per 30 giorni | Consigliato | Test di integrazione |
| REQ-006 | Il dispositivo può mostrare lo stato della sincronizzazione (sincronizzato, invio in corso, conflitto presente) | Consigliato | Ispezione visiva |
