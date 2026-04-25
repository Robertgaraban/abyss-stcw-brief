# Publication Boundary

## Why a boundary is necessary

The active ABYSS production tree mixes application code with real operational artifacts.

Examples of material that should not be part of a public repository include:

- local environment files
- runtime secrets
- SQLite files and SQL dumps
- backups
- invoice PDFs and billing artifacts
- generated documents
- raw incident material with operational detail
- deployment-sensitive tooling and runbooks
- local build output and installed dependencies

## Publicly appropriate

For a public repository, what is appropriate is:

| Artifact | Why it is safe to publish |
|----------|--------------------------|
| System description and README | No sensitive data, establishes product framing |
| Architecture summary | Technology choices and topology, no secrets |
| Module inventory | Module names and status, no implementation detail |
| Curated production-hardening summary | Incident categories without operational residue |
| Platform expansion status | Strategic direction without implementation internals |
| Lifecycle and SGC analytics docs | API shapes and schema descriptions without live data |
| Role model and permission matrix | Access model without live user records |
| Prompt library | Engineering thinking artifacts without operational wiring |
| Screenshots policy | Capture rules without actual sensitive captures |

## Not publicly appropriate

What is not appropriate is:

| Artifact | Why it should stay private |
|----------|---------------------------|
| Full production source tree | Mixes application code with secrets and config |
| Database dumps or exports | Contains operational data |
| Screenshots with live data | Student, billing, or audit records visible |
| Raw post-mortems | Internal operational wiring and URLs |
| Deployment runbooks | Infrastructure and credential paths |
| Worker configs with endpoints | Sensitive integration targets |

## Correct repository model

The correct model for ABYSS is:

```
public brief (this repo)
    └─ README, architecture, module map, role model,
       production hardening, platform expansion, lifecycle,
       SGC analytics, prompts, publication boundary

private cleaned source repo (by request)
    └─ frontend source tree
    └─ backend source tree
    └─ schema and migrations
    └─ workers
    └─ sanitized deployment tooling
    └─ selective post-mortem detail
```

## How to request private access

- Email: **robertgaraban@gmail.com** — Subject: `[Acceso repo privado] abyss-stcw-private`
- GitHub: [Robertgaraban](https://github.com/Robertgaraban)
- LinkedIn: [linkedin.com/in/robertgaraban](https://www.linkedin.com/in/robertgaraban)
