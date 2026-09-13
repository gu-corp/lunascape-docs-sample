---
navigation:
  order: 20
---

# 4.2 Solicitud y respuesta

## POST /notes/push

```json
{
  "id": "n_01HZ3K8Q7V",
  "baseVersion": 4,
  "body": "Compras\n- Leche\n- Huevos",
  "deviceId": "d_macbook"
}
```

Respuesta (correcta):

```json
{ "id": "n_01HZ3K8Q7V", "version": 5, "conflict": false }
```

Respuesta (conflicto: se devuelve el resultado de aplicar [las reglas de 3.4](../03-architecture/conflicts.md)):

```json
{ "id": "n_01HZ3K8Q7V", "version": 6, "conflict": true, "body": "Compras\n- Leche\n- Huevos\n>>> d_iphone\n- Pan" }
```
