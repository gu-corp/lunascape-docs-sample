---
navigation:
  order: 20
---

# 1.2 Alcance y supuestos

## Alcance

| N.º | Dentro del alcance | Fuera del alcance |
|---|---|---|
| 1 | Sincronización de la creación, la actualización y la eliminación de notas | Edición colaborativa de notas (cursores compartidos en la edición simultánea) |
| 2 | Detección y resolución de conflictos entre dispositivos | El editor dentro del dispositivo |
| 3 | La API de sincronización (HTTP) | Facturación y gestión de cuentas |

## Supuestos

- Los dispositivos solo se conectan de forma intermitente. Se da por supuesta la edición sin conexión.
- El cuerpo de una nota tiene un límite de 1 MB.
- El orden no depende del reloj del dispositivo: lo determinan los números de versión del servidor.
