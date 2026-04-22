# Architecture

## Active ABYSS runtime

ABYSS is the active SaaS runtime used to operate the live STCW training organization. The public brief describes it as a product platform with current production depth, not as a lightweight internal tool.

The stack in the working system is:

- frontend SPA in `React + Vite`
- backend API in `Express`
- operational data in `PostgreSQL`
- background workers for queues and scheduled automation jobs
- JWT authentication with RBAC guards
- VPS-oriented backend operation with a separate app delivery path

## Runtime topology

The deployed runtime joins multiple business domains inside one controlled system:

- commercial and admissions flows
- student records and lifecycle flows
- course templates, instances, and academic operations
- attendance, assistance, and evaluation flows
- certifications and verification flows
- billing and finance-related flows
- communications and background processing
- reporting and management KPIs
- student portal
- ISO/SGC quality processes

## Multi-user runtime split

ABYSS is also split by user surface, not only by business domain:

- internal operations shell for staff roles
- dedicated student portal for self-service access
- utility/public views for login, reset, certificate preview/verify, and invoice verification

The runtime root routes users into different visual shells depending on authentication state and role. This is a meaningful product-level distinction, not a cosmetic one.

## Core runtime flow

1. Users access the app shell.
2. The SPA consumes the API with JWT auth and RBAC checks.
3. Backend middleware protects admin, portal, and verification flows according to route type.
4. Services operate on PostgreSQL-backed business entities and traceable workflow state.
5. Workers process queued emails, scheduled reports, reminders, and automation jobs.

## Admin surface and self-service surface

The application shell mounts a broad module surface behind RBAC:

- dashboard
- students
- leads
- courses
- career packs
- career plans
- resources
- attendance
- assistance
- certifications
- invoicing
- communications
- tasks
- manual review
- reports
- users
- settings
- SGC

The broader product surface also includes:

- student portal flows
- certificate verification
- invoice verification
- password reset and access recovery

This is one of the clearest signs that ABYSS is a serious product runtime and not a one-feature system.

## Backend layers

The backend is organized around:

- routes
- services
- middleware
- utils
- migrations
- workers and jobs

These layers support business areas such as:

- pricing and billing
- communications and notifications
- permissions and RBAC
- academic and student operations
- document and certificate flows
- quality and audit-oriented controls

## Frontend layers

The frontend is organized around:

- auth and app-state contexts
- service clients by module
- operational components by business area
- shared UI primitives
- portal-oriented components for student flows

## Operational maturity

ABYSS shows production maturity through more than feature breadth:

- post-mortems exist for real production incidents
- authentication failures were diagnosed and corrected
- quiz timing and scoring regressions were resolved
- communications processing includes worker-oriented controls
- quality and SGC workflows are connected to real business operations

See [Production Hardening](./production-hardening.md).

## Growth model

ABYSS should be understood as a delivered SaaS runtime with a clear expansion path, not as an unfinished concept.

The public framing is:

- ABYSS is the product
- STCW España is the live operating reference
- the system already runs broad real-world operations today
- further school/country scaling is a platformization path built on top of a functioning core, not a substitute for one

That distinction matters because it preserves technical honesty without underselling the maturity that already exists.
