---
navigation:
  order: 30
---

# 3.3 Números de versión

El número de versión es un entero monótonamente creciente que el servidor asigna a cada nota. El dispositivo envía como `baseVersion` la última versión que recibió. Cuando la versión actual del servidor no coincide con `baseVersion`, se considera un conflicto (REQ-003). Los relojes de los dispositivos no intervienen en la determinación del orden ([ORB-ADR-0001](../05-decisions/0001-sync-method.md)).
