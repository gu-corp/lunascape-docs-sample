---
navigation:
  order: 40
---

# 3.4 Resolución de conflictos

| Caso | Regla |
|---|---|
| La misma línea se modificó por separado | Se conservan ambos cambios: el que llegó después se añade al final, separado por `>>>`. Se muestra al usuario que hay un conflicto (REQ-006) |
| Se modificaron líneas distintas | Se integran automáticamente mediante una fusión a tres bandas; no se avisa al usuario |
| Una de las partes lo eliminó | Prevalece la eliminación y el contenido de la otra parte va a la Papelera (REQ-005) |

En todos los casos no se pierde contenido (REQ-004).
