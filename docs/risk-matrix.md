# Practice Software Testing Toolshop
# Risk-Based Testing & Risk Matrix — no. 3

## 1. Purpose

This document defines how the QA project prioritizes testing based on risk.

Risk is used to decide **what should be tested first and most deeply**. It does not prove that a feature is defective.

This project uses the requirements baseline from no. 2. Requirements marked **Proposed / To Verify** remain unconfirmed until they are executed against the application.

---

## 2. Risk Model

### Impact

| Level | Meaning |
|---|---|
| Critical | Failure can prevent a core business transaction, create incorrect financial/order data, or block release-critical functionality. |
| High | Failure significantly affects a major user workflow, account access, data integrity, or important functionality. |
| Medium | Failure affects a meaningful but non-core workflow or causes a moderate usability/functionality problem. |
| Low | Failure has limited functional impact and a practical workaround exists. |

### Likelihood

| Level | Meaning |
|---|---|
| High | Likely to be encountered because the workflow is common, input-heavy, or has many validation paths. |
| Medium | Reasonably possible but less frequent or dependent on a specific condition. |
| Low | Uncommon condition or low-frequency path. |

### Risk

Risk is considered using **Impact × Likelihood**.

| Impact \ Likelihood | Low | Medium | High |
|---|---:|---:|---:|
| Critical | High | Critical | Critical |
| High | Medium | High | Critical |
| Medium | Low | Medium | High |
| Low | Low | Low | Medium |

### Risk response

- **Critical:** test first; prioritize positive, negative, boundary and data-consistency coverage.
- **High:** test early and include regression coverage.
- **Medium:** cover during planned functional/regression testing.
- **Low:** cover when practical; focus on representative cases.

---

## 3. Requirement Risk Prioritization

The following is a **test-planning assessment**, not a claim that a defect exists.

| Requirement Area | Representative Requirements | Impact | Likelihood | Risk | Testing Focus |
|---|---|---|---|---|---|
| Authentication | REQ-AUTH-001 to REQ-AUTH-007 | High | High | Critical | Login, invalid credentials, required fields, logout/session behavior |
| Registration | REQ-REG-001 to REQ-REG-014 | High | High | Critical | Required fields, email, password rules, invalid data, duplicate account |
| Products | REQ-PROD-* | High | Medium | High | Listing, details, price, availability, images |
| Search | REQ-SEARCH-* | Medium | High | High | Matching, no-result, empty/whitespace, partial/case behavior |
| Categories/Filters/Sorting | REQ-CAT-* / REQ-FILTER-* | Medium | Medium | Medium | Filter combinations, clear, sort order |
| Cart | REQ-CART-001 to REQ-CART-008 | High | High | Critical | Add/remove, quantity, totals, multiple products, empty state |
| Checkout | REQ-CHECKOUT-001 to REQ-CHECKOUT-008 | Critical | High | Critical | Required data, totals, unsuccessful checkout, order creation |
| Account | REQ-ACCOUNT-001 to REQ-ACCOUNT-003 | Medium | Medium | Medium | Access, profile display/update |
| Orders | REQ-ORDER-001 to REQ-ORDER-003 | High | Medium | High | History, details, consistency |
| Non-functional | REQ-NFR-001 to REQ-NFR-006 | Medium | Medium | Medium | Usability, viewport, browsers, accessibility, input handling |

**Important:** If a feature is not present in the current application, its related planned coverage must be marked **Not Applicable** or **Not Implemented/To Verify** during execution rather than being treated as a failure.

---

## 4. Testing Priority

### Priority 1 — Release-critical

1. Application availability and core navigation
2. Authentication
3. Registration
4. Product selection/details
5. Cart calculations and state
6. Checkout and order creation
7. Order data consistency

### Priority 2 — High-value functional

1. Search
2. Categories
3. Filters
4. Sorting
5. Account/profile workflows
6. Negative validation paths

### Priority 3 — Supporting quality

1. Responsive behavior
2. Browser compatibility
3. Accessibility checks
4. Usability and validation-message clarity
5. Lower-frequency edge cases

---

## 5. Release Risk

Release risk should be discussed using evidence from executed tests.

Do not write:

> "Release is unsafe because we think checkout may fail."

Write:

> "Release risk remains open because the checkout critical-path tests have not yet been executed."

After execution, release risk should consider:
- number of failed critical/high-priority tests
- severity of confirmed defects
- whether critical workflows are blocked
- defect reproducibility
- regression coverage
- unresolved requirements
- environment limitations
- known application constraints

---

## 6. Risk Review Rules

1. Risk priority can change after execution evidence is available.
2. Severity describes the impact of an observed defect; it is not the same as test priority.
3. Priority describes how urgently the QA team should test or address something.
4. A high-risk requirement does not mean the feature is defective.
5. Hypothetical defects must never be reported as actual defects.
