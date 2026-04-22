# Prompt — Integración WhatsApp

```md
Actúa como arquitecto de integraciones de ABYSS.

Diseña y documenta la integración de `WhatsApp` dentro de ABYSS como una capacidad productiva, no como un addon superficial.

Contexto:
- ABYSS ya tiene módulos de leads, alumnos, soporte, comunicaciones, tareas, reportes y portal.
- La integración debe servir para ventas, seguimiento, soporte, recordatorios y comunicación operativa.
- La solución debe respetar `RBAC`, trazabilidad, idempotencia, colas y auditoría.

Quiero que desarrolles:

1. Casos de uso prioritarios:
- captación comercial
- seguimiento de leads
- recordatorios de documentación
- avisos de cursos / cambios / asistencia
- soporte y conversación operativa
- notificaciones relevantes al alumno

2. Diseño técnico:
- proveedor recomendado
- webhook inbound
- cola outbound
- tabla de conversaciones / mensajes
- normalización de plantillas
- idempotencia
- estados de entrega
- reintentos
- observabilidad

3. Integración con módulos ABYSS:
- leads
- students
- support
- communications
- tasks
- reports

4. Seguridad y cumplimiento:
- consentimiento
- opt-in / opt-out
- retención
- protección de datos
- límites de envío

5. Documentación a producir:
- diagrama de flujo
- tabla de eventos
- endpoints
- modelo de datos
- runbook de fallos
- qué parte mostrar públicamente y qué parte dejar privada

6. Prioridad:
- quick wins
- mínimo producto operativo
- mejoras de segunda fase

Formato:
- Objetivo
- Casos de uso
- Arquitectura
- Modelo de datos
- Flujos
- Riesgos
- Plan de implementación
- Plan documental
```
