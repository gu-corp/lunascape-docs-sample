---
navigation:
  order: 30
---

# 3. Arquitectura

La sincronización se compone de cuatro elementos: el cliente, la API de sincronización, el almacén y las notificaciones ([componentes](components.md)). En [el flujo de sincronización](sync-flow.md) se indica el orden en que un cambio llega del dispositivo al servidor y del servidor a los demás dispositivos. Ese orden se basa en los [números de versión](versioning.md), y el tratamiento de dos actualizaciones que coinciden sobre la misma versión se define en [la resolución de conflictos](conflicts.md).
