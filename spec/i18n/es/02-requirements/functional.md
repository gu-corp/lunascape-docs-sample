---
navigation:
  order: 10
---

# 2.1 Requisitos funcionales

| ID | Requisito | Prioridad | Verificación |
|---|---|---|---|
| REQ-001 | Una nota creada en un dispositivo llega a los demás dispositivos en un plazo de 10 segundos tras la conexión | Obligatorio | Prueba de integración |
| REQ-002 | Una nota editada sin conexión se envía automáticamente al reconectarse | Obligatorio | Prueba de integración |
| REQ-003 | Dos actualizaciones sobre la misma versión se detectan como un conflicto | Obligatorio | Prueba unitaria |
| REQ-004 | El conflicto se resuelve automáticamente con [las reglas de 3.4](../03-architecture/conflicts.md), sin perder el contenido de ninguna de las dos partes | Obligatorio | Prueba unitaria |
| REQ-005 | La eliminación se propaga a los demás dispositivos y se puede restaurar desde la Papelera durante 30 días | Recomendado | Prueba de integración |
| REQ-006 | El dispositivo puede mostrar el estado de sincronización (sincronizado, enviando, con conflicto) | Recomendado | Inspección visual |
