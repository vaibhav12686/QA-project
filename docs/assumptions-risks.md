# Assumptions and Risks

## 1. Purpose

This document records assumptions and risks that may affect the QA project.

## 2. Assumptions

### A1 — Public Demo Application

The Practice Software Testing Toolshop is treated as a public demonstration/testing application.

### A2 — Application Behavior Can Change

The application may change during the 14-day project.

Therefore, locators, workflows and documented behavior must be verified before automation.

### A3 — Test Data

Test accounts and test data may be subject to application reset or environmental changes.

Tests should avoid depending unnecessarily on permanent data.

### A4 — API Availability

The official API is publicly documented, but endpoint availability and actual behavior must be verified through execution.

### A5 — Database

No production database access is assumed.

Database testing will use a local demonstration database.

### A6 — External Services

External systems such as payment providers or email services are not assumed to be directly testable unless the application exposes observable behavior for them.

## 3. Project Risks

| Risk | Impact | Likelihood | Mitigation |
|---|---|---|---|
| Application changes during project | High | Medium | Revalidate locators and workflows |
| Public environment unavailable | High | Medium | Record outage and avoid fabricating results |
| Test data changes/reset | Medium | Medium | Generate controlled test data |
| API/UI behavior differs | High | Medium | Test actual behavior and document mismatch |
| Authentication state becomes invalid | Medium | Medium | Use reusable authentication setup |
| Brittle selectors | High | Medium | Prefer stable Playwright locators |
| Flaky tests | High | Medium | Use proper waits and diagnostics |
| Excessive automation | Medium | Medium | Automate only high-value scenarios |
| Scope becomes too large | High | Medium | Maintain 14-day scope |
| Lack of production DB access | Medium | High | Use local database demonstration |

## 4. Risk-Based Testing Principle

Testing priority should increase when:

- Business impact is high
- Failure probability is high
- Functionality is frequently used
- Functionality is difficult to recover from
- Defects would affect major user journeys

## 5. Important Limitation

The project must never claim:

- Production database validation
- Defects that were not reproduced
- API endpoints that were not verified
- Test results that were not actually executed

## 6. Evidence Rule

Any actual defect included in project documentation must be supported by reproducible evidence.

If an example is created only for educational purposes, it must be labelled:

HYPOTHETICAL / SAMPLE DEFECT