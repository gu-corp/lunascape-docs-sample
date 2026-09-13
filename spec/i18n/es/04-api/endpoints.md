---
navigation:
  order: 10
---

# 4.1 Puntos de conexión

| Método | Ruta | Propósito | Requisito |
|---|---|---|---|
| POST | `/notes/push` | Enviar un cambio de una nota | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | Recibir los cambios posteriores a la versión indicada | REQ-001 |
| DELETE | `/notes/{id}` | Eliminar una nota (enviarla a la papelera) | REQ-005 |
| POST | `/notes/{id}/restore` | Restaurar una nota desde la papelera | REQ-005 |
