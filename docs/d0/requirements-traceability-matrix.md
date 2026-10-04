# Requirements Traceability Matrix

**Project:** AISYS RFID-Enabled Library Solution
**Stage:** D0 — Initiation and Controls
**Status:** Baseline
**Data Classification:** Synthetic data only

---

## 1. Purpose

This Requirements Traceability Matrix (RTM) establishes the initial traceability between the requirements defined in the AISYS Software Development SOP, the planned system components, and the methods that will be used to verify them.

The RTM will be updated throughout the project as requirements are refined, implemented, tested, and demonstrated.

No production library data, credentials, restricted systems, or live institutional environments will be used.

---

# 2. Functional Requirements

| ID   | Requirement                                                                                                               | Planned Implementation / Component             | Verification Method                   | Acceptance Scenario    | Status  |
| ---- | ------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- | ------------------------------------- | ---------------------- | ------- |
| FR01 | Core ILMS functions including cataloguing, members, circulation, fines, holds/reservations and configurable library rules | Library Management module                      | Functional/API tests                  | AC03, AC04             | Planned |
| FR02 | Web-based user interface with search, filtering and role-appropriate workflows                                            | Web UI + REST API                              | UI and API tests                      | AC08                   | Planned |
| FR03 | RFID interoperability through a middleware/adapter layer without direct dependence on physical hardware                   | RFID middleware + mock device adapters         | Integration tests using mock adapters | AC02, AC03, AC05, AC06 | Planned |
| FR04 | Circulation workflows including checkout, renewal, check-in and restriction handling                                      | Circulation service                            | Functional and integration tests      | AC03, AC04             | Planned |
| FR05 | RFID tagging and association of RFID tags with bibliographic/item records                                                 | RFID tagging module                            | Functional/API tests                  | AC02                   | Planned |
| FR06 | Inventory operations using handheld-reader workflows including missing/misplaced item detection                           | Inventory service + handheld RFID mock         | Integration/functional tests          | AC05                   | Planned |
| FR07 | Security-gate event processing and unauthorized movement handling                                                         | Gate-event service + mock gate/CCTV adapters   | Integration tests                     | AC06                   | Planned |
| FR08 | Operational dashboard and reporting                                                                                       | Dashboard/reporting module                     | Functional/report validation tests    | AC08                   | Planned |
| FR09 | Notifications through email/SMS integration boundaries                                                                    | Notification service + mock email/SMS adapters | Integration tests                     | AC06                   | Planned |
| FR10 | Controlled migration of spreadsheet records with validation, staging, rejection and reconciliation                        | Migration pipeline + staging tables            | Migration tests and reconciliation    | AC01                   | Planned |
| FR11 | Administration including users, roles, configuration and audit-related controls                                           | Administration/RBAC module                     | Functional/security tests             | AC07                   | Planned |
| FR12 | Offline installation, update, upgrade and rollback support                                                                | Offline deployment/update package              | Installation and recovery tests       | AC09                   | Planned |

*Requirement scope is based on FR01–FR12 in the AISYS SOP.*

---

# 3. Non-Functional Requirements

| ID    | Requirement                                                           | Planned Implementation / Control                                                          | Verification Method       | Status  |
| ----- | --------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ------------------------- | ------- |
| NFR01 | Preserve data integrity and prevent unintended corruption or deletion | Validation, transactions, backups, migration controls and reconciliation                  | Data-integrity tests      | Planned |
| NFR02 | Security and privacy controls                                         | RBAC, least privilege, audit logging, synthetic/masked data and secure configuration      | Security/control tests    | Planned |
| NFR03 | Compatibility with Windows 11 clients and Windows Server 2022+        | Supported deployment configuration and compatibility testing                              | Environment verification  | Planned |
| NFR04 | Licensing compliance                                                  | Dependency inventory, license review and documentation                                    | Dependency/license review | Planned |
| NFR05 | Testability                                                           | Modular services, mock adapters and automated tests                                       | Automated test execution  | Planned |
| NFR06 | Maintainability                                                       | Layered architecture, documented interfaces, code quality controls and meaningful commits | Code/design review        | Planned |
| NFR07 | Supportability                                                        | Operational documentation, diagnostics, backup/recovery and offline support procedures    | Operational verification  | Planned |
| NFR08 | Documentation                                                         | Requirements, architecture, deployment, administration, user and support documentation    | Documentation review      | Planned |
| NFR09 | Delivery according to the defined D0–D10 process                      | Stage deliverables, reviews and traceability                                              | Stage-gate review         | Planned |

*Requirement scope is based on NFR01–NFR09 in the AISYS SOP.*

---

# 4. Acceptance Scenario Traceability

| Scenario | Acceptance Objective                                                                                                | Related Requirements | Planned Verification                   | Status  |
| -------- | ------------------------------------------------------------------------------------------------------------------- | -------------------- | -------------------------------------- | ------- |
| AC01     | Stage spreadsheet records, reject invalid/duplicate records, migrate valid records and reconcile results            | FR10, NFR01          | Migration test + reconciliation report | Planned |
| AC02     | Validate bibliographic/item information and associate an item with a mocked RFID tag                                | FR03, FR05           | RFID mock integration test             | Planned |
| AC03     | Perform checkout, renewal and check-in through mocked NCIP/SIP2 boundaries and record audit information             | FR03, FR04, NFR02    | Integration + audit verification       | Planned |
| AC04     | Enforce circulation restrictions                                                                                    | FR01, FR04           | Functional test                        | Planned |
| AC05     | Perform handheld inventory scanning and identify missing/misplaced items with visible/audible confirmation          | FR03, FR06           | Mock handheld integration test         | Planned |
| AC06     | Process unauthorized gate events, record accession information and trigger mock CCTV/email actions                  | FR03, FR07, FR09     | Integration test                       | Planned |
| AC07     | Authenticate using smart-card workflow and enforce role-based access control                                        | FR11, NFR02          | Authentication/RBAC test               | Planned |
| AC08     | Display dashboard information and generate required reports                                                         | FR02, FR08           | UI/report validation                   | Planned |
| AC09     | Install/update/rollback the application using offline lifecycle procedures                                          | FR12, NFR03, NFR07   | Offline deployment/recovery test       | Planned |
| AC10     | Restore from backup following a simulated failed migration/integration and demonstrate original data remains intact | NFR01, NFR07         | Backup/restore + integrity test        | Planned |

*Acceptance scenarios are based on AC01–AC10 in the AISYS SOP.*

---

# 5. Architecture Traceability

The planned solution will follow the architecture layers specified by the SOP:

| Architecture Layer | Planned Responsibility                                     | Related Requirements                     |
| ------------------ | ---------------------------------------------------------- | ---------------------------------------- |
| User               | Web interface and role-specific workflows                  | FR02, FR08, FR11                         |
| Application        | Library business logic and workflows                       | FR01, FR04, FR05, FR06, FR08, FR10, FR11 |
| RFID Middleware    | Device abstraction and RFID workflow orchestration         | FR03, FR05, FR06, FR07                   |
| Interoperability   | NCIP 2.0 adapter boundary and SIP2 boundary                | FR03, FR04                               |
| Data               | Library, RFID, circulation, audit and migration data       | FR01, FR05, FR10, NFR01                  |
| Integration        | Email, SMS, CCTV and other external integration boundaries | FR07, FR09                               |
| Operations         | Installation, updates, backup/recovery and administration  | FR11, FR12, NFR07                        |

The SOP specifies these seven architecture layers and requires the RFID/device integrations to be represented through adapter boundaries and mocks where live devices/services are unavailable.

---

# 6. Deliverable Traceability

| Deliverable                     | Purpose                                        | Related Requirements        | Status  |
| ------------------------------- | ---------------------------------------------- | --------------------------- | ------- |
| D1 — Requirements Package       | Requirements baseline and traceability         | FR01–FR12, NFR01–NFR09      | Planned |
| D2 — Architecture Package       | Architecture and interface design              | FR03, NFR05, NFR06          | Planned |
| D3 — Working Prototype          | Demonstrable application foundation            | FR01–FR12                   | Planned |
| D4 — Source Repository          | Controlled source and engineering history      | NFR05, NFR06                | Planned |
| D5 — Database/Migration Package | Database schema and migration controls         | FR10, NFR01                 | Planned |
| D6 — Test Package               | Test cases, results and evidence               | All applicable requirements | Planned |
| D7 — Deployment Package         | Installation/update/rollback materials         | FR12, NFR03, NFR07          | Planned |
| D8 — Operational Documentation  | Administration, support and user documentation | NFR07, NFR08                | Planned |
| D9 — Demonstration              | Demonstration of required workflows            | AC01–AC10                   | Planned |

The SOP defines these mandatory deliverables as part of the expected project outcome.

---

# 7. Verification Status Legend

| Status         | Meaning                                                                    |
| -------------- | -------------------------------------------------------------------------- |
| Planned        | Requirement identified but implementation/verification is not yet complete |
| In Progress    | Implementation or verification has started                                 |
| Verified       | Requirement has been successfully tested and evidence recorded             |
| Blocked        | Verification cannot proceed because of an identified dependency/blocker    |
| Not Applicable | Requirement has been formally determined not to apply, with justification  |

---

# 8. RTM Maintenance Rules

The RTM will be maintained throughout the project.

When a requirement changes, the corresponding design, implementation, test and documentation references will be reviewed and updated together.

Implementation and verification status will not be marked as complete without corresponding evidence.

Changes will be tracked through the repository issue tracker and controlled through reviewed changes.

The RTM will be reviewed at relevant stage gates before progressing to subsequent development stages.

---

## 9. D0 Baseline

**Baseline Date:** 2026-10-04

**Baseline Status:** Initial requirements traceability established.

**Next Review:** D1 Requirements Review

**Current Implementation Status:** Not yet started.

**Data/Credentials:** Synthetic data and credentials only.
