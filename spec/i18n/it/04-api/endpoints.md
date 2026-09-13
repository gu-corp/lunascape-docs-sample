---
navigation:
  order: 10
---

# 4.1 Endpoint

| Metodo | Percorso | Scopo | Requisito |
|---|---|---|---|
| POST | `/notes/push` | Inviare una modifica a una nota | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Ricevere le modifiche successive alla versione indicata | REQ-001 |
| DELETE | `/notes/{id}` | Eliminare una nota (nel cestino) | REQ-005 |
| POST | `/notes/{id}/restore` | Ripristinare una nota dal cestino | REQ-005 |
