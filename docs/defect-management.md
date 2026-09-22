# Practice Software Testing Toolshop
# Defect Management — no. 3

## 1. Purpose

This document defines how defects are identified, documented, prioritized, tracked and communicated in the QA project.

### Evidence rule

The sample defects in this document are **HYPOTHETICAL TRAINING EXAMPLES ONLY**.

They were not recorded as actual defects and must not be reported as defects found in the Practice Software Testing Toolshop.

An actual defect may be created only after:
1. the relevant test case is executed;
2. the observed behavior differs from the expected result;
3. the behavior is reproducible or the limitation is documented;
4. sufficient evidence is captured.

---

## 2. Professional Defect Workflow

**New → Triaged → Assigned → In Progress → Fixed → Retest → Closed**

Possible alternate states:
- Reopened
- Rejected / Not a Bug
- Duplicate
- Cannot Reproduce
- Deferred

### New
QA has documented an observed problem with enough evidence for triage.

### Triaged
The team has reviewed severity, priority, ownership and reproducibility.

### Assigned
The issue has an identified owner.

### In Progress
Development is investigating or implementing a fix.

### Fixed
Development reports that the issue has been corrected.

### Retest
QA verifies the correction.

### Closed
QA confirms the expected behavior and closes the defect.

---

## 3. Severity vs Priority

### Severity

Severity describes **technical/business impact** if the defect is confirmed.

| Severity | Meaning |
|---|---|
| Critical | Core transaction is blocked, major data integrity issue, or severe security/business impact. |
| High | Major functionality is broken with significant user/business impact. |
| Medium | Important functionality is affected but a workaround may exist. |
| Low | Minor functional, visual or usability issue. |

### Priority

Priority describes **how urgently the defect should be addressed**.

| Priority | Meaning |
|---|---|
| P1 | Immediate attention; affects critical release workflow. |
| P2 | High attention; should be addressed in the current cycle where practical. |
| P3 | Normal/lower urgency; can be scheduled with other work. |

Severity and priority are independent. A visually minor issue can have high priority in a particular release, while a technically serious issue may be deferred because of release context.

---

## 4. Professional Bug-Writing Rules

A good bug report should be:

- specific
- reproducible
- evidence-based
- concise
- neutral
- testable
- free from assumptions

### Title formula

**[Area] + [Action/Condition] + [Observed Problem]**

Weak:
> Login broken

Better:
> Login form accepts an invalid credential combination and does not display validation feedback

The second title identifies the area, condition and observable behavior without guessing the implementation cause.

---

## 5. Required Defect Fields

Every actual defect should contain:

- Bug ID
- Title
- Environment
- Precondition
- Steps
- Expected
- Actual
- Severity
- Priority
- Evidence
- Status
- Assignee
- Reproducibility

Optional but useful:
- Requirement ID
- Scenario ID
- Test Case ID
- Build/version
- Browser/device
- Timestamp
- Logs
- Screenshots/video
- Regression status

---

# 6. HYPOTHETICAL SAMPLE DEFECTS — NOT ACTUAL FINDINGS

## BUG-SAMPLE-001 — Hypothetical

**Title:** [Authentication] Invalid credentials are accepted  
**Environment:** Example only — Chrome, desktop, current test build  
**Precondition:** A registered test account exists  
**Steps:**
1. Open the login page.
2. Enter a valid username/email.
3. Enter an intentionally invalid password.
4. Submit the login form.

**Expected:** The application rejects the invalid credentials and provides appropriate feedback.

**Actual:** **Hypothetical example only:** The application signs the user in despite the invalid password.

**Severity:** Critical  
**Priority:** P1  
**Evidence:** None — hypothetical example; no screenshot/log is claimed.  
**Status:** Sample only / Not Reported  
**Assignee:** Unassigned  
**Reproducibility:** Not tested

---

## BUG-SAMPLE-002 — Hypothetical

**Title:** [Registration] Password below the documented minimum is accepted  
**Environment:** Example only — Chrome, desktop  
**Precondition:** Registration page is available  
**Steps:**
1. Open registration.
2. Enter otherwise valid registration data.
3. Enter a password shorter than 8 characters.
4. Submit the form.

**Expected:** The password is rejected because the documented rule requires at least 8 characters.

**Actual:** **Hypothetical example only:** Registration proceeds with the shorter password.

**Severity:** High  
**Priority:** P1  
**Evidence:** None — hypothetical example.  
**Status:** Sample only / Not Reported  
**Assignee:** Unassigned  
**Reproducibility:** Not tested

---

## BUG-SAMPLE-003 — Hypothetical

**Title:** [Cart] Cart total does not reflect updated quantity  
**Environment:** Example only — Chrome, desktop  
**Precondition:** A product is present in the cart and quantity modification is supported  
**Steps:**
1. Open the cart.
2. Change the product quantity.
3. Observe the item subtotal and order total.

**Expected:** Applicable totals are recalculated according to the updated quantity.

**Actual:** **Hypothetical example only:** The displayed total remains unchanged.

**Severity:** High  
**Priority:** P1  
**Evidence:** None — hypothetical example.  
**Status:** Sample only / Not Reported  
**Assignee:** Unassigned  
**Reproducibility:** Not tested

---

## BUG-SAMPLE-004 — Hypothetical

**Title:** [Checkout] Required customer information can be submitted empty  
**Environment:** Example only — Chrome, desktop  
**Precondition:** Checkout is available  
**Steps:**
1. Add a product to the cart.
2. Start checkout.
3. Leave a required customer field empty.
4. Submit the checkout form.

**Expected:** The application prevents submission and identifies the missing required information.

**Actual:** **Hypothetical example only:** Checkout submission succeeds without the required field.

**Severity:** High  
**Priority:** P1  
**Evidence:** None — hypothetical example.  
**Status:** Sample only / Not Reported  
**Assignee:** Unassigned  
**Reproducibility:** Not tested

---

## BUG-SAMPLE-005 — Hypothetical

**Title:** [Orders] Order history shows data different from the submitted order  
**Environment:** Example only — Chrome, desktop  
**Precondition:** A successful order exists  
**Steps:**
1. Open order history.
2. Open the relevant order.
3. Compare product, quantity and total with the submitted order.

**Expected:** Order information remains consistent with the submitted order.

**Actual:** **Hypothetical example only:** The displayed quantity differs from the submitted quantity.

**Severity:** High  
**Priority:** P1  
**Evidence:** None — hypothetical example.  
**Status:** Sample only / Not Reported  
**Assignee:** Unassigned  
**Reproducibility:** Not tested

---

## BUG-SAMPLE-006 — Hypothetical

**Title:** [Accessibility] Form control has no usable accessible name  
**Environment:** Example only — supported browser with accessibility inspection  
**Precondition:** Relevant form is available  
**Steps:**
1. Open the form.
2. Inspect key interactive controls using browser accessibility tooling.
3. Check whether each control exposes a usable accessible name.

**Expected:** Key controls expose appropriate accessible names/labels where applicable.

**Actual:** **Hypothetical example only:** A key control has no usable accessible name.

**Severity:** Medium  
**Priority:** P2  
**Evidence:** None — hypothetical example.  
**Status:** Sample only / Not Reported  
**Assignee:** Unassigned  
**Reproducibility:** Not tested

---

## 7. Defect Triage Questions

Before creating or escalating an actual defect, ask:

1. Can I reproduce it?
2. What exact environment was used?
3. What requirement/test case does it relate to?
4. What should happen?
5. What actually happened?
6. Can another tester reproduce it?
7. Is there evidence?
8. Is it a product defect, test-data issue, environment issue, configuration issue, or expected behavior?
9. What is the impact?
10. How urgently does it need attention?

---

## 8. Defect Evidence

Useful evidence includes:
- screenshot
- screen recording
- browser console output
- network request/response
- application log
- API response
- test execution result

Never attach invented evidence to a defect.

---

## 9. no. 3 Rule

The project currently contains planned test coverage and sample defect-writing exercises. It does **not** contain confirmed application defects unless the user executes a test and records an observed failure.
