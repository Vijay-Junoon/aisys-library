# D0 — Assumptions

**Project:** AISYS RFID-Enabled Library Solution
**Stage:** D0 — Initiation and Controls
**Status:** Baseline
**Date:** 2026-10-04

---

## 1. Purpose

This document records the assumptions used to establish the initial requirements, architecture and implementation approach for the AISYS RFID-enabled library solution.

These assumptions will be reviewed and updated if additional information becomes available during later project stages.

---

## 2. Project Assumptions

### A01 — Synthetic Data

All library records, member information, RFID identifiers, credentials, transactions, logs and other data used during development and demonstration will be synthetic.

No production personal data will be used.

### A02 — No Production System Access

The solution will be developed and tested without access to the institution's production ILMS, production databases or restricted institutional networks.

### A03 — Mock External Devices

Physical RFID readers, handheld readers, security gates, smart-card readers, cameras and other unavailable external devices will be represented through software adapters and working mock implementations.

### A04 — RFID Adapter Boundary

The application will communicate with RFID devices through an abstraction/middleware layer rather than directly depending on a specific physical device.

This allows the prototype to be developed and demonstrated without requiring physical RFID hardware.

### A05 — ILMS Integration Boundary

The existing ILMS will be treated as an external system.

Where live integration is unavailable, the required integration boundaries will be represented using mock adapters/services.

### A06 — NCIP/SIP2 Boundary

NCIP 2.0 and SIP2 will be treated as interoperability boundaries.

The prototype will demonstrate the required interaction patterns through controlled/mock integrations where live institutional services are unavailable.

### A07 — Spreadsheet Migration Source

The migration workflow will use synthetic spreadsheet records representing an existing library dataset.

The migration process will include staging, validation, rejection handling and reconciliation.

### A08 — Target Environment

The solution will be designed for the operating-system environments specified by the SOP, including Windows 11 client environments and Windows Server 2022 or later.

### A09 — Offline Lifecycle

Installation, update, upgrade and rollback workflows will be designed to operate without depending on continuous internet connectivity.

### A10 — Configuration Outside Source Code

Environment-specific configuration and credentials will be supplied through configuration mechanisms rather than being hard-coded into the source repository.

### A11 — Demonstration Environment

Acceptance scenarios will be demonstrated using a controlled test environment and synthetic data rather than a live institutional environment.

### A12 — Traceability

Requirements, design decisions, implementation, testing and documentation will remain traceable through the repository, issue tracker and requirements traceability matrix.

---

## 3. Assumption Review

These assumptions are initial D0 assumptions.

If an assumption is invalidated or clarified during D1–D8, the assumption record, requirements/design references and affected implementation or test artefacts will be updated through the project's change-control process.

---

## 4. Baseline

**Baseline Date:** 2026-10-04

**Status:** Initial D0 assumptions established.

**Review Point:** D1 Requirements Review
