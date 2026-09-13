---
navigation:
  order: 30
---

# 4.3 Errores

| Estado | Significado | Qué hace el dispositivo |
|---|---|---|
| 400 | Formato de solicitud incorrecto | Deja de enviar y lo registra |
| 401 | Token no válido | Vuelve a autenticarse |
| 409 | Discrepancia de versión (conflicto) | Sustituye con el `body` de la respuesta y muestra un conflicto |
| 413 | Cuerpo de más de 1 MB | Avisa al usuario y no envía |
| 429 | Demasiadas solicitudes | Espera los segundos indicados en `Retry-After` y reenvía |
| 5xx | Fallo del servidor | Reenvía con retroceso exponencial (hasta 5 veces) |
