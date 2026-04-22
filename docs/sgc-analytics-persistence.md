# SGC Analytics Persistence

## Why this matters

ABYSS quality management is not just document storage and audit checklists. The runtime already contains a much deeper analytical layer around quality objectives, satisfaction, documentary completeness, and executive indicators.

The recent platform work adds a persistence layer that makes those analytics more reusable and easier to consume over time.

## What already existed

Before the snapshot layer, the SGC module already operated with:

- advanced dashboard calculations
- KPI semaphores
- Likert-based satisfaction aggregation
- automatic sourcing from operational modules such as academic records and certifications
- DGMM-oriented documentary and compliance flows

This is important because the persistence layer is not starting from zero. It is being added on top of an already rich analytical service.

## What is now verifiable

The current runtime now includes:

- `sgc_analytics_snapshots` as a dedicated persistence table for historical KPI states
- a scheduled analytics materialization job
- read-oriented endpoints for latest state and historical trend retrieval

At public brief level, the correct statement is:

- ABYSS SGC already behaves like an analytical engine
- the platform now also persists analytical states for trend review and faster dashboards

## High-level flow

```mermaid
flowchart TD
    A["Operational SGC + academic data"] --> B["SGC analytical services"]
    B --> C["Snapshot materialization job"]
    C --> D["sgc_analytics_snapshots"]
    D --> E["Read-only analytics endpoints"]
    E --> F["Executive dashboard and trend review"]
```

## What this proves

This persistence layer shows three important things:

- ABYSS is already linking quality and operations at data level
- the product is moving from transactional visibility to historical analytics
- the platform is being prepared for stronger executive reporting and external BI-style consumption

## Precision and current limits

This document also preserves technical honesty.

The public brief should not claim that the analytics layer is completely generalized across all future tenants yet.

The defendable claim is:

- tenant-tagged snapshot persistence already exists
- scheduled materialization already exists
- trend-oriented API support already exists
- further hardening toward more generalized tenant-aware analytics remains an active platform concern

## Related documents

- [Platform Expansion Status](./platform-expansion-status.md)
- [Architecture](./architecture.md)
- [Production Hardening](./production-hardening.md)
