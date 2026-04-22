# ABYSS / STCW Technical Brief

ABYSS is a SaaS platform built and hardened over more than five years to run maritime training operations end to end. It is not a narrow back-office tool and it is not a prototype. It is the working product layer behind lead capture, student lifecycle, academic operations, certifications, invoicing, communications, reporting, student self-service, and ISO/SGC quality management in one integrated system.

This repository is the public technical brief for ABYSS. Its purpose is to make the scope, architecture, operational maturity, and engineering depth reviewable without exposing the production source tree, live datasets, billing artifacts, local secrets, or deployment-sensitive material.

## At a glance

- Product: `ABYSS`
- Delivery model: `operational SaaS for maritime training centers`
- Maturity: `5+ years of development and production iteration`
- Current live reference: `STCW España`
- Functional breadth: `18 documented modules`
- User model: `internal multi-role operations + student self-service portal`
- Stack: `React`, `Vite`, `Express`, `PostgreSQL`
- Runtime support: `JWT auth`, `RBAC`, `workers`, `PM2`, `Nginx/VPS`
- Review model: `public technical brief + private cleaned source review on request`

## What ABYSS does

ABYSS concentrates the operational spine of a maritime training center in one platform:

- lead capture and conversion
- student records and lifecycle management
- course templates, course instances, and academic operations
- attendance, assistance, evaluation, and dossier flows
- certifications, verification, and document-linked controls
- invoicing and finance-related workflows
- communications, workers, and scheduled processing
- reporting, management visibility, and KPIs
- student portal and self-service processes
- ISO/SGC quality, audits, objectives, risks, and DGMM-oriented control

## Why this is a SaaS, not a narrow internal app

ABYSS already behaves as a full operational product for a live training organization. The public brief presents it as such because that is the delivered reality:

- one coherent application shell with broad RBAC-governed module coverage
- backend services, workers, and business flows running in production conditions
- public and self-service flows such as portal access and verification routes
- business-critical modules operating together instead of as disconnected tools
- documented product evolution toward broader school and country reuse without permanent forks

The right public framing is `ABYSS`. `STCW España` is the live operating reference. This brief is intentionally written around the product, its delivered capabilities, and its operational maturity.

## Current module surface

The platform currently documents 18 modules with substantial operational coverage across commercial, academic, compliance, portal, finance, and quality domains:

- Dashboard
- Leads
- Students
- Courses
- Venue Resources
- Career Plans
- Career Packs
- Academic Management
- Technical Support
- Certifications
- Invoicing
- Communications
- Tasks
- Reports
- Users and Team
- Settings
- Student Portal
- Quality and SGC

See [Module Map](./docs/module-map.md).

## Role model and user surfaces

ABYSS is not a single-panel tool. It separates internal operations from student self-service and enforces access through role-aware UI and backend authorization.

Core internal roles documented in the runtime:

- `admin`
- `sales`
- `instructor`
- `coordinator`
- `support`
- `student`

In addition, some sensitive operational and quality flows are explicitly protected for specialized roles such as `compliance`, `direction`, and guarded super-admin paths.

The runtime currently exposes three main visual surfaces:

- `internal operations shell` for administration, sales, academic operations, finance, support, reports, and quality
- `student portal shell` for profile, courses, quizzes, documents, certificates, invoices, messages, and support
- `public/utility views` for login, password reset, certificate preview/verification, and invoice verification

See [Role Model](./docs/role-model.md) and [Visual Surface](./docs/visual-surface.md).

## Operational maturity

One of the strongest signals in ABYSS is that it has not only breadth of modules, but also depth of production hardening:

- resolved authentication incidents and routing regressions
- resolved quiz and timeout defects affecting real student flows
- communications workers and automation safety controls
- invoice and certification verification flows
- documented post-mortems and operational fixes instead of ad-hoc patching
- quality/SGC coverage linked to real academic and documentary operations

This matters because serious software is not defined only by how many screens it has. It is defined by how it behaves under load, failure, change, and recovery in a live operation.

See [Production Hardening](./docs/production-hardening.md).

## Architecture summary

The active ABYSS runtime follows a production-oriented full-stack architecture:

- `React SPA` frontend
- `Express API` backend
- `PostgreSQL` operational database
- workers for communications and scheduled jobs
- JWT-based authentication and RBAC
- VPS-oriented backend operations with separate app delivery

High-level runtime view:

```mermaid
flowchart TD
    A["Users"] --> B["React SPA"]
    B --> C["JWT / RBAC"]
    B --> D["Operational Modules"]
    D --> E["Leads / Students / Courses"]
    D --> F["Certifications / Billing / Reports"]
    D --> G["Communications / Portal / SGC"]
    B --> H["Express API"]
    H --> I["PostgreSQL"]
    H --> J["Workers / Queues / Automations"]
```

See [Architecture](./docs/architecture.md).

## Why this repository exists

The production working tree is too sensitive to publish directly. It mixes software layers with material that should not be made public, such as:

- local environment files and secrets
- billing artifacts and generated documents
- database files, dumps, and operational exports
- deployment-sensitive configuration and runbooks
- raw incident material with operational detail

For a serious evaluation, the correct model is:

- public technical brief for orientation
- private cleaned source repository for controlled review

See [Publication Boundary](./docs/publication-boundary.md).

## Evaluation path

If you are reviewing ABYSS:

1. Read this README as the system brief.
2. Review [Architecture](./docs/architecture.md).
3. Review [Module Map](./docs/module-map.md).
4. Review [Role Model](./docs/role-model.md).
5. Review [Visual Surface](./docs/visual-surface.md).
6. Review [Production Hardening](./docs/production-hardening.md).
7. Review [Publication Boundary](./docs/publication-boundary.md).

## Review access

If deeper technical review is required, the next step is controlled access to the private cleaned repository rather than broader public publication of the production tree.

Contact:

- GitHub: [Robertgaraban](https://github.com/Robertgaraban)
- LinkedIn: [linkedin.com/in/robertgaraban](https://www.linkedin.com/in/robertgaraban)

## Notes

- This repository is a technical brief and due-diligence layer for ABYSS.
- It is not an open-source release of the production implementation.
- See [Architecture](./docs/architecture.md), [Module Map](./docs/module-map.md), [Role Model](./docs/role-model.md), [Visual Surface](./docs/visual-surface.md), [Production Hardening](./docs/production-hardening.md), [Publication Boundary](./docs/publication-boundary.md), and [Closeout](./docs/closeout.md).
