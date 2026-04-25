# Prompt — Integración de Plataforma de Pago

```md
Actúa como principal engineer para pagos en ABYSS.

Quiero diseñar y documentar una integración de plataforma de pago para ABYSS, conectada con cursos, alumnos, facturación, certificados y operación administrativa.

Contexto:
- ABYSS ya tiene facturación, alumnos, leads, cursos, certificaciones y portal alumno.
- La integración no debe quedarse en "cobrar"; debe impactar estado de alumno, inscripción, documentos y operación.
- El sistema debe contemplar trazabilidad y validación de negocio.

Necesito:

1. Casos de uso:
- pago de matrícula
- pago parcial
- pago por plan o pack
- conciliación
- reembolso
- impago / vencido
- activación de acceso tras pago

2. Diseño técnico:
- proveedor recomendado y por qué
- checkout / payment link / webhook
- tablas y estados
- reconciliación
- idempotencia
- fallos y reintentos
- firma de webhooks

3. Integración con ABYSS:
- leads → student
- invoice → payment
- enrollment
- portal alumno
- certificación bloqueada si no procede
- soporte / incidencias de pago

4. RBAC y operativa:
- qué puede hacer admin
- qué puede hacer ventas
- qué puede hacer coordinación
- qué ve el alumno

5. Documentación de alto impacto:
- arquitectura
- secuencia webhook→estado→acción
- lifecycle del pago
- matriz de estados
- riesgos
- frontera pública / privada

6. Roadmap:
- MVP
- hardening
- reporting y analítica

Formato:
- Resumen
- Casos de uso
- Arquitectura
- Eventos y estados
- Integración funcional
- Riesgos
- Roadmap
- Artefactos documentales recomendados
```
