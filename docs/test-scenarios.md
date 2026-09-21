# Practice Software Testing Toolshop
# Test Scenarios — Day 2

## Purpose

These scenarios provide high-level coverage between requirements and detailed test cases.

Each scenario should answer:

> **What behavior or quality characteristic are we validating?**

Detailed execution steps belong in `test-cases.xlsx`.

## Scenario Catalog

| Scenario ID | Requirement ID | Module | Scenario |
|---|---|---|---|
| TS-AUTH-001 | REQ-AUTH-001 | Authentication | Verify login page and authentication entry point. |\n| TS-AUTH-002 | REQ-AUTH-002 | Authentication | Verify authentication with valid registered credentials. |\n| TS-AUTH-003 | REQ-AUTH-003 | Authentication | Verify authentication with invalid credentials. |\n| TS-AUTH-004 | REQ-AUTH-004 | Authentication | Verify required-field validation on login. |\n| TS-AUTH-005 | REQ-AUTH-005 | Authentication | Verify logout and transition out of authenticated state. |\n| TS-AUTH-006 | REQ-AUTH-006 | Authentication | Verify session behavior during navigation and after logout. |\n| TS-AUTH-007 | REQ-AUTH-007 | Authentication | Verify unsuccessful-login feedback. |\n| TS-REG-001 | REQ-REG-001 | Registration | Verify registration form availability and field presence. |\n| TS-REG-002 | REQ-REG-002 | Registration | Verify first-name input. |\n| TS-REG-003 | REQ-REG-003 | Registration | Verify last-name input. |\n| TS-REG-004 | REQ-REG-004 | Registration | Verify date-of-birth input and format handling. |\n| TS-REG-005 | REQ-REG-005 | Registration | Verify country selection. |\n| TS-REG-006 | REQ-REG-006 | Registration | Verify postal code and house number. |\n| TS-REG-007 | REQ-REG-007 | Registration | Verify street, city and state fields. |\n| TS-REG-008 | REQ-REG-008 | Registration | Verify phone number input. |\n| TS-REG-009 | REQ-REG-009 | Registration | Verify email input. |\n| TS-REG-010 | REQ-REG-010 | Registration | Verify documented password rules. |\n| TS-REG-011 | REQ-REG-011 | Registration | Verify invalid and incomplete registration submissions. |\n| TS-REG-012 | REQ-REG-012 | Registration | Verify duplicate-account handling. |\n| TS-REG-013 | REQ-REG-013 | Registration | Verify registration validation feedback. |\n| TS-REG-014 | REQ-REG-014 | Registration | Verify country/address relationship where applicable. |\n| TS-PROD-001 | REQ-PROD-001 | Products | Verify product listing displays available products. |\n| TS-PROD-002 | REQ-PROD-002 | Products | Verify product details page/content. |\n| TS-PROD-003 | REQ-PROD-003 | Products | Verify product discovery/navigation. |\n| TS-PROD-004 | REQ-PROD-004 | Products | Verify price consistency between product views. |\n| TS-PROD-005 | REQ-PROD-005 | Products | Verify stock/availability representation. |\n| TS-PROD-006 | REQ-PROD-006 | Products | Verify product image display. |\n| TS-PROD-007 | REQ-PROD-007 | Products | Verify product description display. |\n| TS-PROD-008 | REQ-PROD-008 | Products | Verify navigation from listing to product details. |\n| TS-SEARCH-001 | REQ-SEARCH-001 | Search | Verify search control and search workflow. |\n| TS-SEARCH-002 | REQ-SEARCH-002 | Search | Verify search for a matching product/term. |\n| TS-SEARCH-003 | REQ-SEARCH-003 | Search | Verify no-result search behavior. |\n| TS-SEARCH-004 | REQ-SEARCH-004 | Search | Verify empty search behavior. |\n| TS-SEARCH-005 | REQ-SEARCH-005 | Search | Verify whitespace handling. |\n| TS-SEARCH-006 | REQ-SEARCH-006 | Search | Verify case variation handling where applicable. |\n| TS-CAT-001 | REQ-CAT-001 | Categories | Verify category navigation. |\n| TS-CAT-002 | REQ-CAT-002 | Categories | Verify products displayed after category selection. |\n| TS-CAT-003 | REQ-CAT-003 | Categories | Verify category result relevance. |\n| TS-FILTER-001 | REQ-FILTER-001 | Filters | Verify available filter controls. |\n| TS-FILTER-002 | REQ-FILTER-002 | Filters | Verify individual filter application. |\n| TS-FILTER-003 | REQ-FILTER-003 | Filters | Verify combined filters where supported. |\n| TS-FILTER-004 | REQ-FILTER-004 | Filters | Verify clearing filters. |\n| TS-SORT-001 | REQ-SORT-001 | Sorting | Verify available sorting options. |\n| TS-SORT-002 | REQ-SORT-002 | Sorting | Verify result order for a selected sort. |\n| TS-SORT-003 | REQ-SORT-003 | Sorting | Verify changing sorting order. |\n| TS-CART-001 | REQ-CART-001 | Cart | Verify adding a product to cart. |\n| TS-CART-002 | REQ-CART-002 | Cart | Verify cart contents after adding a product. |\n| TS-CART-003 | REQ-CART-003 | Cart | Verify removing a product. |\n| TS-CART-004 | REQ-CART-004 | Cart | Verify quantity modification. |\n| TS-CART-005 | REQ-CART-005 | Cart | Verify item and order total calculation. |\n| TS-CART-006 | REQ-CART-006 | Cart | Verify cart with multiple products. |\n| TS-CART-007 | REQ-CART-007 | Cart | Verify empty-cart behavior. |\n| TS-CART-008 | REQ-CART-008 | Cart | Verify cart persistence/navigation behavior. |\n| TS-CHECKOUT-001 | REQ-CHECKOUT-001 | Checkout | Verify checkout initiation. |\n| TS-CHECKOUT-002 | REQ-CHECKOUT-002 | Checkout | Verify required customer-field validation. |\n| TS-CHECKOUT-003 | REQ-CHECKOUT-003 | Checkout | Verify address validation. |\n| TS-CHECKOUT-004 | REQ-CHECKOUT-004 | Checkout | Verify order summary. |\n| TS-CHECKOUT-005 | REQ-CHECKOUT-005 | Checkout | Verify checkout total. |\n| TS-CHECKOUT-006 | REQ-CHECKOUT-006 | Checkout | Verify unsuccessful checkout handling. |\n| TS-CHECKOUT-007 | REQ-CHECKOUT-007 | Checkout | Verify successful order creation. |\n| TS-CHECKOUT-008 | REQ-CHECKOUT-008 | Checkout | Verify payment validation where supported. |\n| TS-ACCOUNT-001 | REQ-ACCOUNT-001 | Account | Verify access to supported account functionality. |\n| TS-ACCOUNT-002 | REQ-ACCOUNT-002 | Account | Verify profile information display. |\n| TS-ACCOUNT-003 | REQ-ACCOUNT-003 | Account | Verify profile updates where supported. |\n| TS-ORDER-001 | REQ-ORDER-001 | Orders | Verify order history. |\n| TS-ORDER-002 | REQ-ORDER-002 | Orders | Verify order details. |\n| TS-ORDER-003 | REQ-ORDER-003 | Orders | Verify order data consistency. |\n| TS-NFR-001 | REQ-NFR-001 | Non-functional | Verify navigation usability across core workflows. |\n| TS-NFR-002 | REQ-NFR-002 | Non-functional | Verify core workflow usability at supported viewport sizes. |\n| TS-NFR-003 | REQ-NFR-003 | Non-functional | Verify core workflows across supported browsers. |\n| TS-NFR-004 | REQ-NFR-004 | Non-functional | Verify clarity of validation feedback. |\n| TS-NFR-005 | REQ-NFR-005 | Non-functional | Verify basic accessible naming/labeling of controls. |\n| TS-NFR-006 | REQ-NFR-006 | Non-functional | Verify safe handling of inappropriate input. |\n
## Coverage Categories

### Authentication
- Valid authentication
- Invalid authentication
- Required-field validation
- Session behavior
- Logout
- Unsuccessful-login feedback

### Registration
- Form structure
- Individual input fields
- Email validation
- Password rules
- Boundary values
- Invalid/incomplete registration
- Duplicate registration
- Validation feedback
- Country/address relationship

### Products
- Listing
- Product details
- Product discovery
- Price consistency
- Availability
- Images
- Descriptions
- Navigation

### Search
- Search control
- Matching result
- No result
- Empty input
- Whitespace
- Case variation
- Partial search

### Categories / Filters / Sorting
- Category navigation
- Category relevance
- Filter application
- Combined filters
- Clearing filters
- Sorting
- Sorting order changes

### Cart
- Add
- View
- Remove
- Quantity
- Calculations
- Multiple products
- Empty state
- Persistence/navigation behavior

### Checkout
- Checkout initiation
- Required fields
- Address validation
- Order summary
- Total calculation
- Negative checkout behavior
- Successful order
- Payment validation where supported

### Account / Orders
- Account access
- Profile display
- Profile updates
- Order history
- Order details
- Order consistency

### Non-functional
- Navigation usability
- Responsive behavior
- Browser compatibility
- Validation-message clarity
- Basic accessibility

## Scenario Design Rules

1. Scenarios are intentionally higher-level than test cases.
2. Do not treat a scenario as proof that the underlying functionality exists.
3. If a feature is absent from the current application, mark the related scenario as Not Applicable or remove it after verification.
4. A scenario may map to multiple test cases.
5. A test case must map to at least one requirement.
