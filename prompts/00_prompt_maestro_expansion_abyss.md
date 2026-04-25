# Prompt Maestro — Expansión Funcional y Documental de ABYSS

Usa este prompt cuando quieras que un agente o modelo prepare, estructure y documente la siguiente fase de `ABYSS`.

```md
Actúa como principal architect / product engineer de ABYSS.

Contexto:
- ABYSS es una plataforma SaaS para operaciones de formación marítima.
- Ya existe una base funcional madura con frontend `React + Vite`, backend `Express`, base `PostgreSQL`, `JWT`, `RBAC`, `workers`, `portal alumno`, módulos académicos, certificaciones, facturación, comunicaciones, reportes y calidad `SGC`.
- El objetivo ahora no es inventar una app nueva, sino extender y documentar con criterio lo que más valor aporta a evaluadores técnicos, stakeholders y futuros tenants.

Necesito que estructures una propuesta técnica y documental para estas áreas:
- integración con `WhatsApp`
- integración con `plataforma de pago`
- fortalecimiento del sistema de `clientes / leads / alumnos / operación comercial`
- envío de toda la documentación y trazabilidad de `calidad / SGC` hacia una capa de datos analizable
- documentación priorizada por impacto, porque no sabemos qué será más importante para cada revisor

Tu trabajo debe producir:

1. Un mapa de capacidades objetivo por dominio.
2. Un modelo de integración por dominio:
   - actores
   - eventos
   - entradas y salidas
   - tablas o entidades implicadas
   - endpoints o colas necesarias
   - permisos y roles afectados
3. Un backlog por fases:
   - Fase 1: quick wins
   - Fase 2: integración operativa sólida
   - Fase 3: analítica, automatización y escalado
4. Un apartado de riesgos:
   - seguridad
   - datos sensibles
   - cumplimiento
   - duplicidad
   - trazabilidad
   - coste operativo
5. Un plan documental por impacto:
   - qué debe ir al repo público
   - qué debe quedar en repo privado
   - qué merece screenshot sanitizado
   - qué merece diagrama
   - qué merece runbook técnico
6. Una recomendación explícita de prioridades:
   - qué documentar primero para máximo impacto ante CTO / hiring manager / due diligence
   - qué construir primero para valor real de producto

Reglas:
- No rebajes ABYSS a "CRM"; descríbelo como plataforma SaaS multirol.
- No mezcles ABYSS con JJR.
- No inventes módulos si ya existe evidencia de runtime; parte de lo ya construido y extiéndelo.
- Diferencia claramente entre:
  - hecho ya operativo
  - hardening pendiente
  - expansión futura
- Si detectas una frontera entre público y privado, señálala.
- No entregues marketing; entrega ingeniería con criterio de producto.

Formato de salida:
- Resumen ejecutivo
- Arquitectura por dominios
- Backlog por fases
- Riesgos y controles
- Plan documental priorizado
- Recomendación final de siguiente paso
```
