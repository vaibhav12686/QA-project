# Test Strategy

## 1. Objective

The objective of testing is to evaluate the functional quality, reliability and usability of the Practice Software Testing Toolshop application while demonstrating a professional QA engineering process.

Testing will combine:

- Manual testing
- Exploratory testing
- UI automation
- API testing
- SQL validation demonstration
- Cross-browser testing
- Basic accessibility checks
- Basic security-oriented testing

## 2. Testing Approach

The project follows a risk-based testing approach.

Testing effort will be concentrated on business-critical workflows.

Primary flow:

Application
→ Authentication
→ Product Discovery
→ Product Details
→ Cart
→ Checkout
→ Order
→ Account

## 3. Functional Testing

Functional testing will validate observable application behavior such as:

- Authentication
- Registration
- Product discovery
- Search
- Categories
- Product details
- Cart
- Checkout
- Orders
- Account functionality

Only functionality confirmed in the application will become a final requirement.

## 4. Non-Functional Testing

The project will include lightweight checks for:

- Browser compatibility
- Responsive behavior
- Usability
- Basic accessibility
- Basic security-oriented behavior

Full-scale performance testing and penetration testing are outside the project scope.

## 5. Exploratory Testing

Exploratory testing will be used during application discovery and whenever behavior is unclear.

The tester will simultaneously:

- Learn the application
- Identify risks
- Design tests
- Execute tests
- Record observations

## 6. Smoke Testing

A small set of high-value tests will determine whether the application is sufficiently stable for deeper testing.

Examples include:

- Application availability
- Authentication
- Product availability
- Product details
- Cart
- Checkout

The exact smoke suite will be finalized after application exploration.

## 7. Regression Testing

Regression testing will verify that existing functionality remains stable after changes.

Regression coverage will focus on:

- Authentication
- Product functionality
- Search/filter/sort behavior
- Cart
- Checkout
- Orders
- Account functionality

## 8. Retesting

When an actual defect is reported and fixed, the failed scenario will be executed again to verify the fix.

Retesting will be distinguished from regression testing.

## 9. API Testing

The official Toolshop API documentation will be used as the source of API contract information.

API tests will be implemented only for endpoints that can be legitimately verified.

Testing will include, where applicable:

- HTTP methods
- Status codes
- Response structure
- JSON content
- Validation
- Authentication
- Authorization
- Negative cases

## 10. Database Testing

The public application does not provide direct production database access for this project.

Therefore, database validation will be demonstrated using a local database.

The local database will be clearly identified as a demonstration environment and will not be presented as the application's production database.

## 11. Automation Strategy

Automation will focus on:

- Stable workflows
- High-value regression scenarios
- Repetitive checks
- Data-driven scenarios
- Cross-browser validation

Manual testing will remain important for:

- Exploratory testing
- Usability
- Visual investigation
- New/unstable functionality
- Tests where automation provides little value

## 12. Test Environment

Primary environment:

- Public Practice Software Testing Toolshop application
- Python
- Pytest
- Playwright
- Requests
- Git
- GitHub
- GitHub Actions

Additional tools:

- Postman
- SQLite or PostgreSQL
- HTML/Allure reporting

## 13. Entry Criteria

Testing can begin when:

- Application is accessible
- Relevant functionality is available
- Test environment is usable
- Required test data is available
- Requirements or observable behavior are sufficiently understood

## 14. Exit Criteria

Testing can be considered complete when:

- Planned high-priority scenarios have been executed
- Critical defects are addressed or documented
- Regression testing has been completed
- Automation suite is stable
- Test results are documented
- Residual risks are documented

Final release-readiness criteria will be refined later in the project.

## 15. Quality Principles

1. Do not invent requirements.
2. Do not invent defects.
3. Do not fabricate test results.
4. Prefer evidence over assumptions.
5. Prioritize business risk.
6. Automate valuable repetitive work.
7. Keep automation maintainable.
8. Document limitations honestly.