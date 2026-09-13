---
navigation:
  order: 30
---

# 4.3 Errori

| Stato | Significato | Comportamento del dispositivo |
|---|---|---|
| 400 | Formato della richiesta non valido | Interrompere l'invio e registrarlo nel log |
| 401 | Token non valido | Autenticarsi di nuovo |
| 409 | Versione non corrispondente (conflitto) | Sostituire con il `body` della risposta e segnalare un conflitto |
| 413 | Corpo superiore a 1 MB | Avvisare l'utente e non inviare |
| 429 | Troppe richieste | Attendere i secondi indicati in `Retry-After` e inviare di nuovo |
| 5xx | Errore del server | Inviare di nuovo con backoff esponenziale (fino a 5 volte) |
