# Platform Expansion Status

## Why this document exists

ABYSS should not be evaluated only as a broad operational runtime. It is also evolving into a more reusable platform layer for multiple schools, richer lifecycle visibility, and stronger analytics persistence.

This document captures only the expansion claims that are verifiable from the working runtime and the synced technical material as of `2026-04-22`.

## Strategic layer already produced

The current expansion work is not informal. It already has documented technical outputs covering:

- `WhatsApp` channel integration as a planned operational domain
- external payments expansion beyond the current WooCommerce-linked flow
- unified `lead -> student` lifecycle visibility
- documentation prioritized by impact for technical review and due diligence
- SGC conversion from a documentary layer into a more explicit analytical data layer

This matters because the expansion path is being treated as engineering and product work, not as a loose wishlist.

The public brief also exposes a sanitized prompt and strategy layer under [Prompt Library](../prompts/README.md), so reviewers can see not only the runtime depth but also the structured thinking behind the next domains.

## What is verified in the runtime today

### 1. Config-driven expansion base

The runtime already resolves `TENANT_ID` and `COUNTRY_CODE`, loads tenant bootstrap files, and merges them into runtime and identity configuration.

This is the important public claim:

- ABYSS already has a real configuration-driven expansion base
- tenant identity, branding, contact, and fiscal identity can be modeled as packs
- the platformization path is being built on top of a live product, not in place of one

### 2. Second tenant modeled

`JJR Solutions` already exists as a distinct tenant bootstrap with its own:

- display identity
- branding family and colors
- support, billing, and coordination contacts
- Brazilian legal identity and fiscal fields
- document footer and issuer text

This is a meaningful platform signal because it shows the product is no longer framed only around one fixed operating identity.

### 3. Unified lifecycle surface

ABYSS already exposes a customer lifecycle timeline that aggregates events across:

- lead creation
- communications
- enrollments
- payments
- certifications

This closes one of the most important visibility gaps between commercial and academic operations and makes the lifecycle reviewable as a system, not as disconnected modules.

### 4. Persistent SGC analytics

The SGC layer now has verifiable persistence and scheduling around KPI materialization:

- snapshot table for historical KPI storage
- worker job that materializes analytics periodically
- read-oriented endpoints for latest and historical views

This is important because ABYSS quality management is already more than document storage. It is becoming an explicitly queryable analytical layer.

## What this means for public positioning

The correct public framing is now stronger than a simple “operations app”:

- `ABYSS` is a multi-role SaaS runtime already hardened in production
- it now also has a visible expansion track for tenantization, lifecycle unification, and analytical persistence
- `STCW España` remains the live operating reference
- `JJR Solutions` demonstrates the next reusable tenant layer

## Precision and due-diligence limits

This brief intentionally avoids overclaiming.

What it does **not** claim:

- that every multi-tenant concern is already fully generalized and closed
- that all analytics are fully tenant-aware end to end
- that every planned domain in the strategy documents is already live in production

What it **does** claim, because it is defendable:

- the expansion base is real
- a second tenant is already modeled
- lifecycle aggregation is already implemented
- persistent SGC analytics infrastructure already exists
- the product direction is documented with engineering-grade artifacts, not vague roadmap language

## Recommended review order

1. [Architecture](./architecture.md)
2. [Lifecycle Lead to Student](./lifecycle-lead-student.md)
3. [SGC Analytics Persistence](./sgc-analytics-persistence.md)
4. [Role Model](./role-model.md)
5. [Production Hardening](./production-hardening.md)
