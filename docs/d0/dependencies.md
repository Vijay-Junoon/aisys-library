# D0 — Dependencies

**Project:** AISYS RFID-Enabled Library Solution
**Stage:** D0 — Initiation and Controls
**Status:** Baseline
**Date:** 2026-10-04

---

## 1. Purpose

This document records the known dependencies that may affect the development, testing, deployment or demonstration of the AISYS RFID-enabled library solution.

Dependencies will be reviewed during subsequent project stages and updated when their availability or impact changes.

---

## 2. Dependency Register

| ID    | Dependency                           | Type                            | Purpose / Impact                                               | Current Approach                                             | Status                    |
| ----- | ------------------------------------ | ------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------------ | ------------------------- |
| DEP01 | Existing ILMS                        | External System                 | Required for eventual library-system interoperability          | Represented through an integration boundary and mock service | External                  |
| DEP02 | NCIP 2.0 interface                   | Integration Standard / Boundary | Supports interoperability with the library system              | Define adapter boundary; use mock implementation             | External                  |
| DEP03 | SIP2 interface                       | Integration Boundary            | Supports circulation/device interoperability                   | Define SIP2 boundary; use mock implementation                | External                  |
| DEP04 | RFID reader interfaces               | Hardware Integration            | Required for RFID workflows                                    | Use adapter interfaces and mock readers                      | Unavailable for prototype |
| DEP05 | Handheld RFID reader                 | Hardware Integration            | Required for inventory workflows                               | Use mock handheld-reader implementation                      | Unavailable for prototype |
| DEP06 | RFID security gate                   | Hardware Integration            | Required for gate-event workflows                              | Use mock gate-event implementation                           | Unavailable for prototype |
| DEP07 | Smart-card reader/workflow           | Hardware Integration            | Required for smart-card authentication workflow                | Use controlled/mock implementation                           | Unavailable for prototype |
| DEP08 | CCTV integration                     | External Integration            | Required for security-event workflow                           | Use mock CCTV adapter                                        | Unavailable for prototype |
| DEP09 | Email service                        | External Integration            | Required for notification workflow                             | Use mock email adapter                                       | Unavailable for prototype |
| DEP10 | SMS service                          | External Integration            | Required for notification workflow                             | Use mock SMS adapter                                         | Unavailable for prototype |
| DEP11 | Synthetic migration spreadsheet      | Data                            | Required to demonstrate controlled migration                   | Create controlled synthetic dataset                          | Available/To be created   |
| DEP12 | Database system                      | Software                        | Stores application and operational data                        | Use development/test database                                | Planned                   |
| DEP13 | Application runtime and dependencies | Software                        | Required to execute the application                            | Pin and document project dependencies                        | Planned                   |
| DEP14 | Windows 11 client environment        | Operating System                | Required compatibility target                                  | Verify application behavior on supported client environment  | Planned                   |
| DEP15 | Windows Server 2022+ environment     | Operating System                | Required server compatibility target                           | Verify deployment approach against supported environment     | Planned                   |
| DEP16 | Offline deployment/update package    | Deployment                      | Required for offline lifecycle operations                      | Create controlled offline package                            | Planned                   |
| DEP17 | Backup and restore mechanism         | Operations                      | Required for recovery and data-integrity verification          | Implement and test backup/restore workflow                   | Planned                   |
| DEP18 | Git repository and issue tracker     | Engineering                     | Required for source control, traceability and project controls | Git repository + issue tracking                              | Available                 |
| DEP19 | Automated testing framework          | Engineering                     | Required for repeatable verification                           | Establish automated test suite                               | Planned                   |
| DEP20 | Dependency/license information       | Engineering                     | Required for licensing and maintainability controls            | Maintain dependency inventory and license information        | Planned                   |

---

## 3. External Dependencies

The following dependencies are outside the direct control of the prototype development team:

* Existing institutional ILMS
* Production NCIP/SIP2 services
* Physical RFID hardware
* Smart-card hardware
* CCTV infrastructure
* Institutional email/SMS services
* Production deployment infrastructure
* Institution-specific security and operational policies

Because these dependencies may not be available, the prototype will use controlled interfaces and mock implementations where appropriate.

---

## 4. Dependency Management

Dependencies that become available or unavailable during development will be recorded and reviewed.

Where an external dependency cannot be accessed:

1. Define the required interface.
2. Implement a mock or controlled test implementation.
3. Keep the application logic independent of the external implementation.
4. Test the integration boundary.
5. Document the limitation.

This approach allows development and verification to continue without access to production systems or physical devices.

---

## 5. Engineering Dependencies

Project dependencies will be:

* Pinned to known versions where practical.
* Reviewed for licensing implications.
* Documented for reproducibility.
* Included in the project's dependency inventory.
* Considered for offline installation requirements.

The SOP specifically requires pinned dependencies, SBOM/license information and offline notes as part of the engineering controls.

---

## 6. Baseline

**Baseline Date:** 2026-10-04

**Status:** Initial D0 dependency register established.

**Review Point:** D1 Requirements Review
