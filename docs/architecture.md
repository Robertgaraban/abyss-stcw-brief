# Architecture

## Active runtime

The active runtime is `CRM-STCW`.

The architecture documented in the working system is:

- frontend SPA in `React + Vite`
- backend API in `Express`
- operational data in `PostgreSQL`
- background workers for queues and automation jobs
- JWT authentication with RBAC guards
- VPS-oriented backend operation with a separate app delivery path

## Core runtime flow

1. Users access the app shell.
2. The SPA consumes the API with JWT auth.
3. Backend middleware enforces access except for public or verification routes.
4. Services operate on PostgreSQL-backed business entities.
5. Workers process queued emails, assistance notifications, and scheduled automation work.

## Backend layers

- routes
- services
- utils
- migrations
- workers and jobs

These layers support business areas such as:

- pricing
- billing
- communications
- permissions and RBAC
- academic/student operations
- document and certificate flows

## Frontend layers

- contexts for auth and app state
- service clients by module
- operational components by business area
- shared UI primitives

## Platform extraction direction

The codebase documents an explicit platform direction toward:

- reusable core logic
- better tenant boundary definition
- reduced hardcoding
- country and tenant configuration separation

That direction is important, but it should be described as `in progress`, not as already complete in the current runtime.

## Engineering signal

From a portfolio and technical-review perspective, this architecture demonstrates:

- full-stack delivery under production constraints
- broad domain coverage in one operational system
- architectural thinking beyond single-feature development
- evidence of platformization work on top of a live business runtime
