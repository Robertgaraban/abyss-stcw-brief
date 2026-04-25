# Lifecycle Lead to Student

## Why this matters

One of the clearest signs that ABYSS is a serious operating platform is that the customer journey is not split across unrelated tools.

The lifecycle already spans commercial, academic, finance, and certification touchpoints. The current platform work makes that journey reviewable in one place.

## Lifecycle model

```mermaid
flowchart LR
    A["Contacto / Lead"] --> B["Cualificación comercial"]
    B --> C["Conversaciones y seguimiento"]
    C --> D["Conversión a alumno"]
    D --> E["Matrícula / curso"]
    E --> F["Pago / facturación"]
    F --> G["Portal alumno"]
    G --> H["Certificación"]
```

## What is already implemented

The current runtime already includes a unified timeline surface for customers.

Verified elements:

- backend endpoint: `GET /api/v1/customers/:id/timeline`
- permission gate: current access is protected through read permission on the commercial side
- frontend component: `CustomerTimeline.jsx`
- event aggregation across multiple domains using one chronological response

## Event types already covered

The timeline currently consolidates these event classes:

| Event type | Source domain | What it represents |
|------------|--------------|-------------------|
| `lead_created` | Commercial | Initial contact record created |
| `message` | Communications | Follow-up or campaign communication sent |
| `enrollment` | Academic | Student enrolled in a course or career plan |
| `payment` | Invoicing | Payment record linked to enrollment or invoice |
| `certification` | Certifications | Certificate generated or issued after completion |

That means the review surface already crosses module boundaries instead of showing isolated CRUD records.

## API contract summary

```
GET /api/v1/customers/:id/timeline

Authorization: Bearer <jwt>
Required permission: leads:read

Response shape:
{
  customer_id: string,
  events: [
    {
      type: "lead_created" | "message" | "enrollment" | "payment" | "certification",
      occurred_at: ISO8601,
      summary: string,
      ref_id: string,
      module: string
    }
  ]
}
```

Events are returned in chronological order. The response is assembled by the backend service layer across multiple tables in a single request.

## Data model behind the timeline

The timeline draws from several operational tables:

| Table | Contributes |
|-------|------------|
| `leads` | Lead creation events |
| `messages` / `communications_log` | Communication events |
| `enrollments` | Enrollment events |
| `invoices` / `payments` | Payment events |
| `certifications` | Certification completion events |

The aggregation is performed server-side. The frontend component renders the result as a chronological feed, not as a set of separate module views.

## Operational meaning

This lifecycle view gives ABYSS a stronger product story because it links:

- admissions and sales follow-up
- academic progression
- billing events
- certification completion

For a reviewer, this is one of the most useful ways to understand that the system behaves like an operational backbone and not like a set of disconnected admin screens.

## Current public interpretation

The public claim should be:

- ABYSS already exposes a lifecycle review surface that connects commercial and academic events
- the journey is visible from first contact to certification
- the implementation exists in both backend and frontend layers

The brief should not claim that every lifecycle state or every channel is fully unified yet. The honest and stronger statement is that the unification work is already real and visible in the runtime.

## Related documents

- [Platform Expansion Status](./platform-expansion-status.md)
- [Architecture](./architecture.md)
- [Role Model](./role-model.md)
