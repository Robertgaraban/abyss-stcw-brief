# Module Map

## Documented module inventory

This public status map is aligned to the current ABYSS planning and audit material, not to older index documents that lag behind module closures and production hardening.

| ID | Module | Status | Domain | Evidence |
|----|--------|--------|--------|----------|
| 00 | Dashboard | Operational | Reporting / KPIs | Audited and closed |
| 01 | Leads | Active | Commercial pipeline | Broad production use |
| 02 | Students | Active | Lifecycle management | Broad production use |
| 03 | Courses | Active | Academic operations | Mature runtime and materials flow |
| 04 | Venue Resources | Active | Calendar / resources | Calendar and instructor/resource coverage |
| 05 | Career Plans | Operational | Academic planning | Functional closure documented |
| 06 | Career Packs | Operational | Bundle management | Functional closure documented |
| 07 | Academic Management | Active | Attendance / evaluation | Attendance, evaluation, records |
| 08 | Technical Support | Active | Support / tickets | Tickets, assignment, comments |
| 09 | Certifications | Operational | Compliance / docs | Generation and verification flow live |
| 10 | Invoicing | Operational | Finance / billing | Billing and verification flow live |
| 11 | Communications | Operational | Async messaging | Workers, bulk actions, monitoring, health |
| 12 | Tasks | Operational | Operations / workflow | CRUD, Kanban, widgets, automation |
| 13 | Reports | Operational | BI / KPIs | Reporting, KPIs, scheduled reports |
| 14 | Users and Team | Operational | Access control | RBAC and permissions matrix |
| 15 | Settings and Configuration | Operational | Platform config | Security, integrations, privacy, profile |
| 16 | Student Portal | Active / improving | Self-service UX | Broad coverage with mobile-first hardening |
| 18 | Quality and SGC | Operational | ISO / compliance | Documentary phase complete, audited |

## Per-module capability depth

### Dashboard (00)
- KPI cards and trend widgets
- Real-time and scheduled data aggregation
- Role-scoped visibility

### Leads (01)
- Lead intake, qualification, and follow-up pipeline
- Communication log and conversion tracking
- Integration with student enrollment flow

### Students (02)
- Full student record with academic and personal data
- Lifecycle events across enrollment, payments, and certifications
- Unified customer timeline from first contact to certification

### Courses (03)
- Course templates and active course instances
- Academic calendar, schedule, and resource assignment
- Linked to attendance, evaluation, and certification flows

### Venue Resources (04)
- Instructor and venue capacity calendar
- Resource conflict detection and scheduling

### Career Plans (05)
- Multi-course academic planning per student
- Linked to enrollment and billing flows

### Career Packs (06)
- Bundled course offerings with pricing logic
- Assignment and lifecycle tracking

### Academic Management (07)
- Attendance tracking per course and session
- Evaluation forms and grade recording
- Dossier management and academic records

### Technical Support (08)
- Ticket system with assignment and thread comments
- Escalation and status tracking

### Certifications (09)
- Certificate generation linked to course completion
- Public verification endpoint for third-party checks
- Document-linked compliance controls

### Invoicing (10)
- Invoice generation and management
- Public verification endpoint
- Finance-linked student and course data

### Communications (11)
- Bulk messaging with worker-based delivery
- Worker health monitoring and retry logic
- Automation safety controls and scheduling

### Tasks (12)
- CRUD task management
- Kanban board view
- Dashboard widgets and automated task triggers

### Reports (13)
- Multi-domain KPI reports
- Scheduled report generation and delivery
- Management visibility surface

### Users and Team (14)
- Role assignment and permission matrix
- Backend RBAC enforcement per module and action
- Audit trail for sensitive operations

### Settings and Configuration (15)
- Platform-wide configuration
- Integration management
- Security settings and privacy controls

### Student Portal (16)
- Mobile-first dedicated student shell
- Own courses, quizzes, materials, documents, certificates
- Invoicing, support, and messages in self-service

### Quality and SGC (18)
- ISO/SGC documentary and audit flows
- Objectives, risks, and DGMM-oriented controls
- Persistent analytics and KPI snapshot layer

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
