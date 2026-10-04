# D0 — Risk Register

**Project:** AISYS RFID-Enabled Library Solution
**Stage:** D0 — Initiation and Controls
**Status:** Baseline
**Date:** 2026-10-04

---

## 1. Purpose

This risk register identifies the major risks known at project initiation that may affect requirements, development, integration, migration, testing, deployment or demonstration.

Risks will be reviewed throughout the project and updated when their probability, impact or mitigation changes.

---

## 2. Risk Register

| ID  | Risk                                                                                    | Probability | Impact | Mitigation / Control                                                                                             | Status |
| --- | --------------------------------------------------------------------------------------- | ----------- | ------ | ---------------------------------------------------------------------------------------------------------------- | ------ |
| R01 | Production ILMS access is unavailable                                                   | High        | High   | Treat ILMS as an external boundary and use mock integration services                                             | Open   |
| R02 | Physical RFID hardware is unavailable                                                   | High        | High   | Define vendor-neutral adapter interfaces and working mock RFID devices                                           | Open   |
| R03 | NCIP/SIP2 live services are unavailable                                                 | High        | High   | Implement integration boundaries and mock NCIP/SIP2 services                                                     | Open   |
| R04 | Production library data is unavailable or restricted                                    | High        | High   | Use synthetic data throughout development and demonstration                                                      | Open   |
| R05 | Migration may corrupt or incorrectly transform records                                  | Medium      | High   | Use staging, validation, rejection handling, reconciliation, backup and restore testing                          | Open   |
| R06 | Duplicate or invalid spreadsheet records may enter the migration pipeline               | Medium      | High   | Validate records before migration and maintain rejected-record/error information                                 | Open   |
| R07 | External device/vendor specifications may change                                        | Medium      | Medium | Isolate device-specific logic behind adapter interfaces                                                          | Open   |
| R08 | Integration failures may affect core library workflows                                  | Medium      | High   | Keep integration boundaries isolated and test them independently with mocks                                      | Open   |
| R09 | Unauthorized access may expose library or user information                              | Medium      | High   | Apply RBAC, least privilege, audit logging and synthetic/masked data controls                                    | Open   |
| R10 | Offline update may fail or leave the application unusable                               | Medium      | High   | Provide controlled update/rollback procedures and test recovery                                                  | Open   |
| R11 | Backup restoration may fail after a migration or integration failure                    | Low/Medium  | High   | Include backup/restore testing and verify original data integrity                                                | Open   |
| R12 | Requirements may change during development                                              | Medium      | Medium | Maintain RTM and apply change control across requirements, design, code, tests and documentation                 | Open   |
| R13 | Dependency/licensing issues may affect delivery                                         | Medium      | Medium | Pin dependencies and maintain dependency/license inventory and offline notes                                     | Open   |
| R14 | Prototype may unintentionally make unsupported interoperability or certification claims | Low         | High   | Clearly document adapter/mock boundaries and avoid unsupported claims about standards, vendors or certifications | Open   |
| R15 | Insufficient test coverage may leave acceptance scenarios unverified                    | Medium      | High   | Map requirements to acceptance scenarios and maintain an automated/manual test package                           | Open   |

---

## 3. High-Priority Risks

### R01 — Production ILMS Unavailable

The assignment excludes access to production systems and databases.

**Mitigation:** Treat the ILMS as an external integration boundary and implement controlled mock services.

---

### R02 — Physical RFID Hardware Unavailable

The assignment does not require physical manufacture, installation or repair of RFID equipment.

**Mitigation:** Implement RFID middleware using adapter interfaces and working mock devices.

---

### R05 — Migration Data Integrity

Migration is a high-impact operation because incorrect transformation could result in inaccurate records.

**Mitigation:**

* Stage imported records.
* Validate records before migration.
* Reject invalid records.
* Detect duplicates.
* Maintain migration errors.
* Reconcile source and migrated records.
* Maintain backup/recovery capability.
* Verify that original data remains intact after simulated failures.

This directly supports acceptance scenarios AC01 and AC10.

---

### R09 — Security and Privacy

Unauthorized access or inappropriate handling of data could compromise the system.

**Mitigation:**

* Use synthetic data.
* Implement role-based access control.
* Apply least-privilege principles.
* Avoid storing secrets in source code.
* Maintain audit information for relevant actions.
* Use masked logs where appropriate.

These controls align with the engineering controls specified by the SOP.

---

### R10 — Offline Lifecycle Failure

The system must support offline installation, update, upgrade and rollback.

**Mitigation:** Package dependencies and deployment artefacts for offline use and explicitly test installation, update and rollback scenarios.

---

## 4. Risk Review Process

Risks will be reviewed at relevant project stage gates.

When a risk changes:

1. Update the risk status.
2. Record the updated mitigation.
3. Identify affected requirements.
4. Identify affected design/implementation components.
5. Update relevant tests and documentation.
6. Record significant changes through the issue tracker.

---

## 5. Risk Status Legend

| Status    | Meaning                                               |
| --------- | ----------------------------------------------------- |
| Open      | Risk is currently active                              |
| Mitigated | Controls have reduced the risk to an acceptable level |
| Accepted  | Risk remains but has been explicitly accepted         |
| Closed    | Risk is no longer applicable                          |
| Escalated | Risk requires external clarification or decision      |

---

## 6. Baseline

**Baseline Date:** 2026-10-04

**Status:** Initial D0 risk register established.

**Review Point:** D1 Requirements Review
