
#  Test Scenario  — Swag Labs E-commerce Application

## 1. Document Information

| Field | Details |
|---|---|
| Project Name | Swag Labs Manual QA Case Study |
| Document ID | SL-TS-001 |
| Version | 1.0 |
| Status | Draft — Pending Test Execution |
| Prepared By | Mashiat Anjum Talukder |
| Application URL | [https://www.saucedemo.com/](https://www.saucedemo.com/) |
| Created Date | 26 October 2026 |
| Test Type | Manual Functional Testing |

## 2. Introduction

This document outlines the high-level test scenarios for the Swag Labs e-commerce web application. The scenarios cover the main user journeys, including authentication, product browsing, shopping cart operations, checkout, order overview, order completion, and application navigation.

The purpose of this document is to identify the functionalities that need to be validated before developing detailed test cases and executing manual tests.

## 3. Test Scenarios by Module

### A. Login Module (`TS_LOG`)

| Scenario ID | Test Scenario Description | Priority |
|---|---|---|
| SL-TS-LOG-001 | Verify successful login using valid credentials for a standard user. | High |
| SL-TS-LOG-002 | Verify login behavior when invalid credentials are entered. | High |
| SL-TS-LOG-003 | Verify validation behavior when both username and password fields are left empty. | High |
| SL-TS-LOG-004 | Verify validation behavior when the username field is left empty and the password is provided. | High |
| SL-TS-LOG-005 | Verify validation behavior when the password field is left empty and the username is provided. | High |
| SL-TS-LOG-006 | Verify that an appropriate error message is displayed when a locked-out user attempts to log in. | Medium |
| SL-TS-LOG-007 | Verify application behavior when logging in with the problem user account. | Medium |
| SL-TS-LOG-008 | Verify application behavior when logging in with the performance glitch user account. | Medium |

### B. Products / Inventory Module (`TS_INV`)

| Scenario ID | Test Scenario Description | Priority |
|---|---|---|
| SL-TS-INV-001 | Verify that the product inventory page loads successfully after valid login. | High |
| SL-TS-INV-002 | Verify that product names, images, descriptions, and prices are displayed correctly. | High |
| SL-TS-INV-003 | Verify product sorting functionality by name in ascending order (A to Z). | Medium |
| SL-TS-INV-004 | Verify product sorting functionality by name in descending order (Z to A). | Medium |
| SL-TS-INV-005 | Verify product sorting functionality by price in ascending order (low to high). | Medium |
| SL-TS-INV-006 | Verify product sorting functionality by price in descending order (high to low). | Medium |
| SL-TS-INV-007 | Verify that the selected sorting option is reflected in the displayed product order. | Medium |

### C. Shopping Cart Module (`TS_CART`)

| Scenario ID | Test Scenario Description | Priority |
|---|---|---|
| SL-TS-CART-001 | Verify that adding a product to the cart updates the cart badge count correctly. | High |
| SL-TS-CART-002 | Verify that adding multiple distinct products updates the cart badge count correctly. | High |
| SL-TS-CART-003 | Verify that removing a product from the inventory page updates the cart badge count correctly. | High |
| SL-TS-CART-004 | Verify that the cart displays the correct selected products, quantities, and prices. | High |
| SL-TS-CART-005 | Verify that a product can be removed from the shopping cart page. | High |
| SL-TS-CART-006 | Verify that the cart badge and cart contents remain consistent after adding and removing products. | High |
| SL-TS-CART-007 | Verify that clicking the "Continue Shopping" button returns the user to the inventory page. | Low |
| SL-TS-CART-008 | Verify that the cart page displays the appropriate state when no products have been added. | Medium |

### D. Product Details Module (`TS_PDT`)

| Scenario ID | Test Scenario Description | Priority |
|---|---|---|
| SL-TS-PDT-001 | Verify that clicking a product name or image opens the corresponding product details page. | High |
| SL-TS-PDT-002 | Verify that the product name, image, description, and price on the details page match the inventory listing. | High |
| SL-TS-PDT-003 | Verify that a product can be added to the cart directly from the product details page. | Medium |
| SL-TS-PDT-004 | Verify that a product can be removed from the cart directly from the product details page when applicable. | Medium |
| SL-TS-PDT-005 | Verify that clicking the "Back to products" button returns the user to the inventory page. | Medium |

### E. Checkout Module (`TS_CHK`)

| Scenario ID | Test Scenario Description | Priority |
|---|---|---|
| SL-TS-CHK-001 | Verify that clicking the checkout button from the cart opens the customer information page. | High |
| SL-TS-CHK-002 | Verify that valid customer information allows the user to proceed to the order overview page. | High |
| SL-TS-CHK-003 | Verify that validation messages are displayed when all required customer information fields are left empty. | High |
| SL-TS-CHK-004 | Verify that validation is performed when the first name field is left empty. | High |
| SL-TS-CHK-005 | Verify that validation is performed when the last name field is left empty. | High |
| SL-TS-CHK-006 | Verify that validation is performed when the ZIP/postal code field is left empty. | High |
| SL-TS-CHK-007 | Verify that clicking the "Cancel" button returns the user to the shopping cart page. | Medium |
| SL-TS-CHK-008 | Verify the checkout behavior when the shopping cart contains no products. | Medium |

### F. Order Overview Module (`TS_OOV`)

| Scenario ID | Test Scenario Description | Priority |
|---|---|---|
| SL-TS-OOV-001 | Verify that the order overview displays the same selected products and quantities as the shopping cart. | High |
| SL-TS-OOV-002 | Verify that product names and individual prices on the overview page match the selected products. | High |
| SL-TS-OOV-003 | Verify that the item subtotal is calculated correctly based on the selected products. | High |
| SL-TS-OOV-004 | Verify that the tax amount is calculated correctly according to the application's displayed pricing rules. | High |
| SL-TS-OOV-005 | Verify that the total price equals the item subtotal plus tax. | High |
| SL-TS-OOV-006 | Verify that clicking the "Cancel" button on the overview page aborts the checkout flow and returns the user to the inventory page. | Medium |

### G. Order Completion Module (`TS_OCM`)

| Scenario ID | Test Scenario Description | Priority |
|---|---|---|
| SL-TS-OCM-001 | Verify that clicking the "Finish" button completes the order when the checkout flow is valid. | High |
| SL-TS-OCM-002 | Verify that the order confirmation page displays the expected confirmation header, "Thank you for your order!". | High |
| SL-TS-OCM-003 | Verify that the order completion page displays the expected order confirmation message. | Medium |
| SL-TS-OCM-004 | Verify that clicking the "Back Home" button redirects the user to the inventory page. | High |
| SL-TS-OCM-005 | Verify that the cart badge and active cart state are cleared after successful order completion. | High |

### H. Navigation Module (`TS_NAV`)

| Scenario ID | Test Scenario Description | Priority |
|---|---|---|
| SL-TS-NAV-001 | Verify that the hamburger side navigation menu opens and closes correctly. | Medium |
| SL-TS-NAV-002 | Verify that the "All Items" menu option navigates to the inventory page. | Medium |
| SL-TS-NAV-003 | Verify the behavior of the "About" menu option. | Medium |
| SL-TS-NAV-004 | Verify that clicking "Logout" ends the user session and redirects to the login page. | High |
| SL-TS-NAV-005 | Verify that the "Reset App State" option resets the application's cart and product-selection state. | Medium |
| SL-TS-NAV-006 | Verify browser back and forward navigation behavior across relevant application pages. | Medium |

## 4. Priority Definitions

| Priority | Definition |
|---|---|
| High | Critical functionality required for core user journeys, authentication, cart management, or checkout. |
| Medium | Important functionality that supports normal application usage but is less critical than the core workflow. |
| Low | Lower-impact functionality that should be validated after higher-priority scenarios. |

## 5. Execution Notes

- These scenarios identify what needs to be tested; detailed steps and test data will be documented separately in the Test Case document.
- Actual results and execution statuses must be recorded only after performing the tests.
- Defects should be reported only when unexpected behavior is observed and reproducible.
- Application behavior should be verified against the current version of the public demo.
- Special demo accounts may exhibit intentionally different behavior; observations should be documented accurately.
- Any scenario that cannot be executed should be marked as Blocked or Not Run, with an explanation in the execution record.

## 6. Document Status

**Prepared By:** Mashiat Anjum Talukder

**Review Status:** Pending Self-Review

**Approval Status:** Not Applicable — Independent Portfolio Project
