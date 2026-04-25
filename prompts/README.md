# Prompt Library — ABYSS

This folder contains the structured engineering and product specification prompts produced as part of the ABYSS expansion work.

These are not marketing materials. They are working artefacts that define architecture, data contracts, integration flows, risk models, and documentation priorities for the next platform domains.

## Why this library is public

Making the prompt library visible in the public brief serves one purpose: it shows that the expansion direction of ABYSS is treated as engineering and product work, not as vague roadmap language.

A reviewer looking at this library can see:

- the level of technical rigour applied to each domain
- the structured thinking behind actors, events, entities, and risks
- the distinction between what is already operational and what is in specification phase

## Contents

| File | Domain | Purpose |
|------|--------|---------|
| `00_prompt_maestro_expansion_abyss.md` | Platform-wide | Master prompt: capabilities map, integration models, phased backlog, risks, documentation plan |
| `01_integracion_whatsapp.md` | WhatsApp | Inbound/outbound messaging, queue design, module integration, compliance |
| `02_integracion_pagos.md` | Payments | Payment lifecycle, webhook handling, state machine, RBAC, reconciliation |
| `03_sistema_clientes_y_operaciones.md` | Customer system | Full lifecycle from lead to alumni, domain model, ownership matrix, integration map |
| `04_sgc_a_datos_y_analitica.md` | Quality / SGC analytics | SGC sources to analytical layer, data model, pipeline, use cases |
| `05_documentacion_por_impacto.md` | Documentation strategy | Prioritization matrix, artifact classification, public vs. private decisions |

## Recommended use order

1. `00_prompt_maestro_expansion_abyss.md` — start here for the full expansion framing
2. `01_integracion_whatsapp.md` — if reviewing communications/messaging domain
3. `02_integracion_pagos.md` — if reviewing payments and billing domain
4. `03_sistema_clientes_y_operaciones.md` — if reviewing commercial and lifecycle domain
5. `04_sgc_a_datos_y_analitica.md` — if reviewing quality and analytics domain
6. `05_documentacion_por_impacto.md` — if reviewing documentation strategy

## Rules of use

These prompts are designed to produce:

- concrete architecture, not generic description
- data contracts and API shapes
- risk and compliance coverage
- phased backlog (quick wins → operational → analytics/scale)
- explicit public vs. private publication decisions
- actionable documentation

They are not for generating marketing copy or vague feature lists.

## Status

All five domain prompts and the master prompt are complete. They represent the current state of ABYSS expansion specification as of `2026-04-25`.
