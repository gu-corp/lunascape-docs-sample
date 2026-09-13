---
navigation:
  order: 10
---

# ORB-ADR-0001: Adoptar «versiones asignadas por el servidor con fusión a tres vías» como método de sincronización

| Elemento | Contenido |
|---|---|
| ID del documento | ORB-ADR-0001 |
| Versión | 1.0 |
| Fecha de actualización | 2026-07-01 |
| Estado | Aprobado |

## 1. Antecedentes

Las notas editadas sin conexión en varios dispositivos deben converger. Se consideraron tres candidatos: (a) prevalece la última modificación según la marca de tiempo, (b) un CRDT, (c) números de versión asignados por el servidor con una fusión a tres vías.

## 2. Decisión

| N.º | Decisión |
|---|---|
| 1 | El orden se decide por el número de versión que asigna el servidor. No se confía en el reloj del dispositivo |
| 2 | Los conflictos se resuelven con una fusión a tres vías; la línea que no se pueda resolver conserva ambas partes. La prioridad es no perder contenido |
| 3 | No se adopta un CRDT: las notas son breves, no hay requisito de edición simultánea y no compensa el coste de duplicar o más el tamaño del cuerpo |

## 3. Consecuencias

| N.º | Consecuencia |
|---|---|
| 1 | El dispositivo conserva `baseVersion` y lo adjunta en cada envío |
| 2 | Mostrar el conflicto (REQ-006) pasa a ser una función obligatoria del dispositivo |
| 3 | El servidor guarda el historial de los últimos 30 días (para la Papelera y como base de las fusiones a tres vías) |
