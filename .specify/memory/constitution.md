# Gestor de Hoja de Vida Institucional Constitution

## Core Principles

### Desarrollo guiado por especificaciones
Toda funcionalidad debe iniciar con requisitos claros, revisados y aprobados antes de planificar la implementación.
El plan técnico y las tareas derivadas deben revisarse y aceptarse antes de comenzar el desarrollo.
Se seguirá el flujo de trabajo de Spec Kit: Constitución → Especificación → Planificación → Tareas → Implementación.

### Calidad y pruebas
El código debe ser modular, mantenible y tipado estrictamente.
Se usarán class‑validator y class‑transformer para la validación de datos.
Cada unidad debe contar con pruebas unitarias automatizadas en Jest; no se declarará una prueba como completada sin evidencia de ejecución.

### Seguridad y protección de datos
Autenticación mediante Passport y JWT, contraseñas hash con bcrypt.
Roles propuestos: FUNCIONARIO, TALENTO_HUMANO y ADMIN – pendientes de validación antes de fijarlos como definitivos.
Protección de datos personales conforme a la normativa vigente; gestión de secretos el mecanismo de gestión de secretos está pendiente de definición.
Se revisará el control de acceso en cada endpoint.

### Trazabilidad de requisitos y gestión de cambios
Cada requisito será registrado en la Spec y vinculado a los tickets de tareas.
Los cambios requerirán revisión de impacto, aprobación del responsable de arquitectura y actualización de la documentación de la Constitución y la Especificación.

### Métricas de IA
Se contempla el uso de speckit‑metricas v0.3.0 para medir esfuerzo, tiempo, costo y código generado por IA.
Su instalación, compatibilidad con Spec Kit y los hooks necesarios deberán verificarse antes de considerarla operativa.

## Tecnologías y arquitectura

- Framework: NestJS
- Lenguaje: TypeScript, Node.js
- Base de datos: PostgreSQL (ORM: Prisma)
- Validación: class‑validator, class‑transformer
- Seguridad: Passport, JWT, bcrypt
- Documentación API: Swagger / OpenAPI
- Pruebas: Jest

> Pendiente: versiones específicas de cada tecnología.

## Flujo de trabajo y criterios de calidad

1. Constitución → define los principios y normas del proyecto.
2. Especificación → requisitos detallados y criterios de aceptación.
3. Planificación → descomposición en tareas y asignación.
4. Tareas → implementación de funcionalidades individuales.
5. Implementación → desarrollo siguiendo los principios; revisión por pares y pruebas automatizadas antes del merge.

**Criterios de calidad**
- Modularidad y separación de responsabilidades.
- Tipado estricto con TypeScript.
- Validación de datos en DTOs.
- Pruebas unitarias y de integración automatizadas.
- Documentación completa vía Swagger.

> Pendiente: definición de CI/CD y pipelines de auditoría.

## Governance

La Constitución es la fuente de verdad; cualquier cambio requiere propuesta escrita y aprobación mediante pull request (una revisión es suficiente).
Las actualizaciones deben incluir registro de versión y fecha de ratificación; si la fecha es desconocida, se marcará como [PENDING_RATIFICATION_DATE].
Se realizará una revisión trimestral de la Constitución para validar su alineación con las decisiones del proyecto.
Las desviaciones de los principios deberán documentarse y ser aprobadas por el responsable de arquitectura.
El cumplimiento se verificará mediante auditorías internas cuando sea necesario, no como obligación para cada release mayor.

**Version**: [PENDING_VERSION] | **Ratified**: [PENDING_RATIFICATION_DATE] | **Last Amended**: 2026-10-22