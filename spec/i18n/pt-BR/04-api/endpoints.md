---
navigation:
  order: 10
---

# 4.1 Endpoints

| Método | Caminho | Finalidade | Requisito |
|---|---|---|---|
| POST | `/notes/push` | Enviar uma alteração de nota | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Receber as alterações posteriores à versão indicada | REQ-001 |
| DELETE | `/notes/{id}` | Excluir uma nota (para a lixeira) | REQ-005 |
| POST | `/notes/{id}/restore` | Restaurar uma nota da lixeira | REQ-005 |
