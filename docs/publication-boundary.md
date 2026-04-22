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

- system description
- architecture summary
- module inventory
- curated production-hardening summary
- technically honest product framing
- controlled review policy

## Not publicly appropriate

What is not appropriate is:

- open publication of the active production tree
- partial dumps from the working data layer
- screenshots or exports with sensitive business data
- raw post-mortems with internal operational wiring
- release of deployment-sensitive tooling without curation

## Correct repository model

The correct model for ABYSS is:

- `public brief`
- `private cleaned source repo`
- `controlled access` for serious evaluation
