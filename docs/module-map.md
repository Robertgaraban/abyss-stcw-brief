# Module Map

## Documented module inventory

This public status map is aligned to the current ABYSS planning and audit material, not to older index documents that lag behind module closures and production hardening.

| ID | Module | Status | Evidence |
|----|--------|--------|----------|
| 00 | Dashboard | Operational | Audited and closed |
| 01 | Leads | Active | Broad production use |
| 02 | Students | Active | Broad production use |
| 03 | Courses | Active | Mature runtime and materials flow |
| 04 | Venue Resources | Active | Calendar and instructor/resource coverage |
| 05 | Career Plans | Operational | Functional closure documented |
| 06 | Career Packs | Operational | Functional closure documented |
| 07 | Academic Management | Active | Attendance, evaluation, records |
| 08 | Technical Support | Active | Tickets, assignment, comments |
| 09 | Certifications | Operational | Generation and verification flow live |
| 10 | Invoicing | Operational | Billing and verification flow live |
| 11 | Communications | Operational | Workers, bulk actions, monitoring, health |
| 12 | Tasks | Operational | CRUD, Kanban, widgets, automation |
| 13 | Reports | Operational | Reporting, KPIs, scheduled reports |
| 14 | Users and Team | Operational | RBAC and permissions matrix |
| 15 | Settings and Configuration | Operational | Security, integrations, privacy, profile |
| 16 | Student Portal | Active / improving | Broad coverage with mobile-first hardening |
| 18 | Quality and SGC | Operational | Documentary phase complete, audited |

## What this proves

ABYSS is not a narrow commercial front end. The runtime covers multiple connected domains:

- commercial pipeline
- student lifecycle
- academic operations
- certifications
- billing
- communications
- reporting
- internal administration
- student self-service
- quality and compliance

That breadth is one of the strongest signals in the project.

## Operational evidence behind the map

The application shell mounts a broad RBAC-governed module inventory, and the wider runtime includes public and self-service flows such as portal access and verification routes. The system is therefore deeper than a public module list alone:

- admin modules are mounted behind permissions
- student portal has dedicated functional coverage
- reporting, communications, invoicing, and SGC are integrated into the same runtime
- the module surface is backed by backend services, workers, migrations, and operational docs

## Important constraint

The module inventory is public. The full implementation of each module is not.

For this project, publishing a reliable module map is appropriate. Publishing the entire operational tree is not.
