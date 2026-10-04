# D0 — Excluded Work

**Project:** AISYS RFID-Enabled Library Solution
**Stage:** D0 — Initiation and Controls
**Status:** Baseline
**Date:** 2026-10-04

---

## 1. Purpose

This document records work that is explicitly excluded from the scope of the AISYS software development assignment.

Excluded work will not be treated as a project defect or incomplete requirement unless the assignment scope is formally changed.

---

## 2. Physical Hardware

The following physical hardware activities are excluded:

* Manufacture of RFID readers.
* Manufacture of RFID gates.
* Manufacture of RFID tags.
* Manufacture of smart cards.
* Manufacture or repair of printers.
* Manufacture or repair of PCs.
* Manufacture or repair of servers.
* Manufacture or repair of cameras.
* Physical cabling work.
* Physical installation of RFID equipment.
* Physical installation or repair of gates, readers or other devices.

The project may define software interfaces and mock implementations for these devices, but does not include their physical manufacture, installation or repair.

---

## 3. Production System Access

The following are excluded:

* Access to production ILMS systems.
* Access to production databases.
* Use of production personal data.
* Access to restricted institutional networks.
* Deployment into a live institutional environment.

Development and demonstration will use controlled environments and synthetic data.

---

## 4. Production Integration

The prototype will not claim to provide a production-ready connection to an institutional ILMS where the required production configuration or service is unavailable.

Instead, the relevant integration boundaries will be defined and demonstrated through controlled/mock implementations.

This includes:

* ILMS integration.
* NCIP 2.0 integration.
* SIP2 integration.
* RFID device integrations.
* Smart-card integration.
* CCTV integration.
* Email integration.
* SMS integration.

---

## 5. Unsupported Claims

The project will not make unsupported claims regarding:

* NCIP certification.
* SIP2 certification.
* ISO certification.
* OEM/vendor certification.
* Security certification.
* Performance certification.
* Production-scale performance guarantees.
* Compatibility with specific hardware or vendor systems where the required hardware/system has not been tested.

The prototype will clearly distinguish between:

1. Implemented functionality.
2. Mocked functionality.
3. Defined integration boundaries.
4. Untested production integrations.

---

## 6. Personal and Restricted Data

The project will not intentionally use:

* Real library member personal information.
* Production circulation records containing personal information.
* Production credentials.
* Institutional authentication credentials.
* Restricted institutional datasets.
* Unapproved personal or confidential information.

Synthetic data will be used for development, testing and demonstration.

---

## 7. Hardware-Dependent Validation

Where physical hardware is unavailable, the project will validate the software workflow through mocks rather than claiming physical-device validation.

Examples include:

* Mock RFID reader.
* Mock handheld RFID reader.
* Mock RFID security gate.
* Mock smart-card reader.
* Mock CCTV integration.
* Mock email service.
* Mock SMS service.

---

## 8. Scope Boundary

The project focuses on developing and demonstrating the software solution, integration boundaries, migration workflow, testing, documentation and operational procedures required by the assignment.

Physical infrastructure procurement, installation, repair and production institutional deployment are outside the project scope.

---

## 9. Baseline

**Baseline Date:** 2026-10-04

**Status:** Initial D0 excluded-work boundary established.

**Review Point:** D1 Requirements Review
