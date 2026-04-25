# Production Hardening

## Why this matters

ABYSS should be evaluated not only by module breadth, but also by how it has been operated, debugged, and stabilized under real production conditions.

The project has documented incident history, corrective work, and operational discipline. That is one of the clearest differences between a prototype and a serious SaaS runtime.

## Representative resolved incidents

| Date | Area | Incident | Outcome |
|------|------|----------|---------|
| 2026-02-26 | Academic / Quizzes | Quizzes showing outdated score on latest attempt | Resolved |
| 2026-02-26 | Academic / Quizzes | Quiz flow hanging when time expired | Resolved |
| 2026-02-12 | Auth / Routing | Duplicated auth routing recurrence | Resolved |
| 2025-12-02 | Auth / API | Total authentication crisis on `/api/auth/*` | Resolved |

## Wider incident record

The documented incident index also covers other production events across frontend delivery, portal access, batch operations, gateway failures, and browser/protocol issues. The public brief does not publish raw operational detail, but it does make clear that ABYSS has been operated through real failure scenarios rather than only greenfield development.

Additional categories in the documented record:

| Category | Examples |
|----------|---------|
| Frontend delivery | Black-screen incidents on SPA load |
| Gateway failures | 502 errors under load or misconfiguration |
| Portal access | Runtime errors blocking student portal entry |
| Batch operations | Certification batch process blocking |
| Access / protocol | Intermittent 401s and HTTP/2 issues |
| Worker reliability | Communications worker retry and health failures |

## Engineering response model

For each documented incident, the response followed a structured pattern:

1. **Detection** — symptom identification through logs, user reports, or monitoring
2. **Isolation** — narrowing the failure to a specific layer (auth, routing, worker, frontend)
3. **Root cause analysis** — tracing the actual cause rather than patching the symptom
4. **Production-safe correction** — resolving without side effects on adjacent flows
5. **Post-mortem** — documented record of what happened, why, and what changed

This is not an informal process. It reflects a production-oriented engineering discipline built up over years of live operation.

## Resilience patterns present in the runtime

| Pattern | Where it applies |
|---------|-----------------|
| JWT refresh and rotation | Auth layer — prevents stale session failures |
| Worker retry and health tracking | Communications and scheduled jobs |
| Route guard redundancy | Frontend and backend access control |
| Schema migration tooling | PostgreSQL — managed, traceable schema evolution |
| PM2 process supervision | Node API and workers — automatic restart on crash |
| Deploy smoke checks | VPS delivery — post-deploy verification before traffic cutover |
| Rollback tooling | VPS delivery — safe reversion on deploy failure |

## What this proves technically

This incident record demonstrates engineering depth in areas that matter for a real business runtime:

- systematic debugging across frontend, backend, and routing layers
- production-safe correction instead of one-off patches
- post-mortem culture and traceability
- resilience work on auth, quizzes, communications, and access flows
- operational confidence built through recovery, not just feature delivery

## Public boundary

The public brief deliberately summarizes maturity without exposing raw incident files, deployment-sensitive data, or live operational residue. For deeper review, the right path remains controlled access to the private cleaned source repository.
