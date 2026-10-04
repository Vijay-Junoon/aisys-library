# D0 — Synthetic Data and Credentials Declaration

**Project:** AISYS RFID-Enabled Library Solution
**Stage:** D0 — Initiation and Controls
**Status:** Baseline
**Date:** 2026-10-04

---

## 1. Purpose

This document formally confirms the data and credential handling approach for the AISYS software development assignment.

The project will use synthetic data and synthetic credentials for development, testing and demonstration.

---

## 2. Synthetic Data Declaration

All data used by the project will be synthetic, generated specifically for development, testing or demonstration purposes.

This includes, but is not limited to:

* Library member records.
* Member names and contact information.
* Book and bibliographic records.
* Item/accession records.
* RFID tag identifiers.
* Circulation transactions.
* Checkout, renewal and check-in records.
* Fine records.
* Reservation/hold records.
* Inventory records.
* RFID inventory scan events.
* Security-gate events.
* CCTV event references.
* Notification records.
* Migration spreadsheet records.
* Audit records.
* Test data.
* Demonstration data.

No production personal information will be intentionally imported into the project.

---

## 3. Credential Declaration

No production or institutional credentials will be used in the project.

Any credentials required for local development, testing or demonstration will be synthetic/test credentials.

Examples include:

* Test administrator accounts.
* Test librarian accounts.
* Test member accounts.
* Mock API credentials.
* Mock RFID-device credentials.
* Mock NCIP/SIP2 credentials.
* Mock email credentials.
* Mock SMS credentials.
* Local database credentials.

Credentials will not be committed directly to the source repository.

---

## 4. Secrets Management

Secrets and environment-specific configuration will be kept outside application source code.

The project will use appropriate configuration mechanisms for local/test environments.

Examples may include:

* Environment variables.
* Local configuration files excluded from version control.
* Test-only credentials.
* Mock authentication tokens.

A template configuration file may be provided where necessary, but it will not contain real secrets.

---

## 5. Logging and Audit Data

Logs and audit records generated during development and testing will use synthetic identifiers and data.

Sensitive information will not be intentionally written to logs.

Where appropriate, logs will use masked or synthetic values.

---

## 6. Production Data and Credentials

The following are explicitly prohibited from the project unless the assignment scope is formally changed and appropriate authorization is provided:

* Production library databases.
* Production member information.
* Production circulation data.
* Institutional authentication credentials.
* Production API keys.
* Production RFID credentials.
* Production email/SMS credentials.
* Production database passwords.
* Restricted institutional datasets.

---

## 7. Demonstration Environment

All demonstrations will use:

* Synthetic library records.
* Synthetic RFID identifiers.
* Test accounts.
* Mock external services.
* Mock RFID devices where required.
* Controlled test scenarios.

The demonstration will not require access to a live institutional environment.

---

## 8. Repository Safety

The repository will not contain:

* Real passwords.
* API keys.
* Access tokens.
* Production database credentials.
* Institutional authentication credentials.
* Private certificates or private keys.

Secret-scanning and dependency/security checks will be considered as part of the project's engineering controls.

---

## 9. Declaration

**I confirm that the AISYS prototype will use synthetic data and synthetic/test credentials for development, testing and demonstration.**

**Production data and production credentials will not be used.**

**Baseline Date:** 2026-10-04

**Status:** Confirmed
