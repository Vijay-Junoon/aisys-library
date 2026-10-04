# D0 — Open Questions

**Project:** AISYS RFID-Enabled Library Solution
**Stage:** D0 — Initiation and Controls
**Status:** Baseline
**Date:** 2026-10-04

---

## 1. Purpose

This document records questions and clarifications that may affect requirements, architecture, implementation, integration, testing or deployment.

Where the assignment does not provide an answer, the project will use the documented D0 assumptions and mock interfaces until clarification becomes available.

---

## 2. Open Questions

| ID  | Question                                                                                                         | Potential Impact                                    | Current Handling                                                                                 | Status |
| --- | ---------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ------ |
| Q01 | What specific existing ILMS product/version will the solution ultimately integrate with?                         | Integration architecture and adapter implementation | Treat ILMS as an external system and use a mock integration boundary                             | Open   |
| Q02 | What exact NCIP 2.0 operations are expected to be supported by the target ILMS?                                  | NCIP adapter scope                                  | Define an adapter boundary and demonstrate required workflows using mocks                        | Open   |
| Q03 | What exact SIP2 operations and message flows are expected?                                                       | SIP2 interoperability implementation                | Maintain SIP2 as an integration boundary and use mocks where live service is unavailable         | Open   |
| Q04 | Which RFID reader/gate/handheld hardware vendors are expected in the target environment?                         | Device adapter implementation                       | Use vendor-neutral adapter interfaces and mock devices                                           | Open   |
| Q05 | What RFID tag technology/frequency and identifier format will be used in the target environment?                 | RFID tag model and validation rules                 | Use a configurable synthetic RFID identifier format for the prototype                            | Open   |
| Q06 | What smart-card technology and authentication mechanism will be used?                                            | Authentication implementation                       | Demonstrate the workflow using a controlled/mock smart-card mechanism                            | Open   |
| Q07 | What CCTV integration interface is expected?                                                                     | Gate-event integration                              | Use a mock CCTV adapter and record the resulting event/action                                    | Open   |
| Q08 | What exact email and SMS providers or institutional services will be used?                                       | Notification integration                            | Use mock notification adapters                                                                   | Open   |
| Q09 | What is the exact schema and column structure of the source spreadsheet for migration?                           | Migration validation and mapping                    | Define a synthetic migration template during requirements/design                                 | Open   |
| Q10 | What library-specific circulation rules, fine policies, loan periods and restriction rules should be configured? | Circulation and policy engine                       | Implement configurable rules using synthetic demonstration policies                              | Open   |
| Q11 | What exact reports and dashboard metrics are required by the target library?                                     | Reporting scope                                     | Implement the reports required by the acceptance scenarios and refine during requirements review | Open   |
| Q12 | What offline update/package distribution mechanism is expected in the target environment?                        | Deployment and lifecycle design                     | Demonstrate an offline package-based installation/update/rollback workflow                       | Open   |
| Q13 | What exact Windows Server 2022+ deployment topology is expected?                                                 | Deployment architecture                             | Design a supported deployment package without assuming a production topology                     | Open   |
| Q14 | What backup/restore mechanism is preferred by the target environment?                                            | Recovery implementation                             | Demonstrate backup and restore using the prototype environment                                   | Open   |
| Q15 | What exact institutional security, retention and audit policies apply?                                           | Security and operational controls                   | Follow the controls stated in the SOP and use synthetic data                                     | Open   |

---

## 3. Questions That Require External Clarification

The following questions cannot be conclusively answered from the supplied assignment alone:

* Target ILMS product and version
* Production NCIP/SIP2 configuration
* Specific RFID hardware vendors and protocols
* RFID tag technology and identifier standards
* Smart-card technology
* CCTV integration mechanism
* Email/SMS provider
* Production spreadsheet schema
* Institution-specific circulation policies
* Institution-specific reporting requirements
* Production deployment topology
* Institutional backup, retention and security policies

These items will remain documented as open until authoritative information is provided.

---

## 4. Current Resolution Strategy

Because production systems, production data, restricted networks and unavailable physical devices are outside the assignment scope, the prototype will not block development on these questions.

Instead:

1. Integration points will be defined through interfaces.
2. Mock implementations will provide working demonstrations.
3. Configuration will be externalized.
4. Synthetic data will be used.
5. Assumptions will be documented.
6. Questions affecting implementation will be revisited during the relevant requirements/design stage.

The SOP explicitly requires adapter interfaces and working mocks when external device/vendor SDK/live services are unavailable.

---

## 5. Baseline

**Baseline Date:** 2026-10-04

**Status:** Initial D0 questions recorded.

**Review Point:** D1 Requirements Review

**Owner:** Development Team
