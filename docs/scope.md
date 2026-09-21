# Testing Scope

## 1. Purpose

This document defines what is included and excluded from the QA project.

## 2. In Scope

### Functional UI Testing

The following areas will be investigated and tested when confirmed in the application:

- Home page
- Product listing
- Product search
- Product categories
- Product details
- Authentication
- Registration
- Shopping cart
- Checkout
- Orders
- Account/profile functionality

### API Testing

The official Practice Software Testing API will be investigated.

Only documented and actually accessible endpoints will be tested.

### Non-Functional Testing

Limited testing will cover:

- Responsive behavior
- Browser compatibility
- Basic accessibility
- Usability
- Basic security-oriented behavior

### Automation

The project will use:

- Python
- Pytest
- Playwright

Automation will focus on stable, repeatable and high-value scenarios.

### Database Demonstration

A local SQLite or PostgreSQL database will be created to demonstrate:

- SELECT
- WHERE
- JOIN
- GROUP BY
- ORDER BY
- COUNT
- SUM
- UI/API/database validation concepts

This database is not the production database of the public application.

## 3. Out of Scope

The following are outside the primary project scope:

- Production database access
- Full penetration testing
- Full performance/load testing
- Stress testing
- Source-code review of the application
- Infrastructure security assessment
- Third-party payment provider testing outside the application
- Email infrastructure testing outside the application
- Administrative functionality unless legitimately accessible
- Features not present in the current application

## 4. Scope Decision Rule

If a feature is not observed in the application or documented by an authoritative project source, it will not automatically be treated as a requirement.

It will instead be marked as:

- Not observed
- Requires confirmation
- Proposed requirement

## 5. Automation Scope

Not every manual test will be automated.

Automation candidates should generally be:

- Repeatable
- Stable
- Business-critical
- Time-consuming when executed manually
- Valuable during regression testing

Exploratory and usability testing will remain primarily manual.

## 6. Evidence

Important failures should have appropriate evidence such as:

- Screenshot
- Test output
- Logs
- Trace
- Video when useful
- API request/response
- SQL result

## 7. Scope Review

Scope will be reviewed whenever significant application behavior is discovered during testing.

The project must adapt to the current application rather than relying on outdated assumptions.