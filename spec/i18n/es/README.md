# Servicio de sincronización de notas Orbit — Especificación funcional

| Elemento | Contenido |
|---|---|
| ID del documento | ORB-SPEC-001 |
| Versión | 1.3 |
| Fecha de actualización | 2026-09-06 |
| Estado | Aprobado |
| Responsable del documento | Equipo de desarrollo de Orbit (ficticio) |
| Relacionados | ORB-REQ-001 (lista de requisitos), ORB-ADR-0001 (elección del método de sincronización) |

## Historial de revisiones

| Versión | Fecha | Contenido de la revisión | Autor |
|---|---|---|---|
| 1.0 | 2026-07-01 | Primera edición | Equipo de desarrollo de Orbit |
| 1.1 | 2026-08-10 | Se añadieron las reglas de resolución de conflictos (3.4) | Equipo de desarrollo de Orbit |
| 1.2 | 2026-09-06 | Se añadió la tabla de errores de la API (4.3) | Equipo de desarrollo de Orbit |
| 1.3 | 2026-09-06 | Se reorganizó en una carpeta por capítulo | Equipo de desarrollo de Orbit |

## Estructura

1. [Descripción general](01-overview/README.md) — objetivo, [alcance y supuestos](01-overview/scope.md), [términos](01-overview/terms.md)
2. [Requisitos](02-requirements/README.md) — [requisitos funcionales](02-requirements/functional.md), [requisitos no funcionales](02-requirements/non-functional.md), [trazabilidad de requisitos](02-requirements/traceability.md)
3. [Arquitectura](03-architecture/README.md) — [componentes](03-architecture/components.md), [flujo de sincronización](03-architecture/sync-flow.md), [número de versión](03-architecture/versioning.md), [resolución de conflictos](03-architecture/conflicts.md)
4. [API](04-api/README.md) — [puntos de conexión](04-api/endpoints.md), [solicitud y respuesta](04-api/push.md), [errores](04-api/errors.md)
5. [Decisiones de diseño](05-decisions/README.md) — [ORB-ADR-0001, elección del método de sincronización](05-decisions/0001-sync-method.md)

> **Acerca de este documento**
> Es una especificación ficticia creada como ejemplo de escritura para Lunascape Docs. Ni el producto ni la empresa existen. Sirve para mostrar el uso de una carpeta por capítulo, tablas, diagramas (Mermaid), código y traducciones.
