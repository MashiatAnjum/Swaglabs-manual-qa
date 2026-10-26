Test Plan — Swag Labs E-commerce Application

## 1. Document Information

| Field | Details |
|---|---|
| Project Name | Swag Labs Manual QA Case Study |
| Document ID | SL-TP-001 |
| Version | 1.0 |
| Status | Draft — pending test execution |
| Prepared By | Mashiat Anjum Talukder |
| Application URL | [https://www.saucedemo.com/](https://www.saucedemo.com/) |
| Created Date | 25 October 2026 |
| Test Type | Manual Functional Testing |

## 2. Introduction

This document defines the scope, objectives, approach, test environment, and completion criteria for manual testing of the Swag Labs e-commerce web application.

The project simulates a basic online shopping experience, allowing a tester to practise validating authentication, product browsing, shopping cart functionality, and checkout workflows.

---

## 3. Objectives

* Validate core shopping workflows from login through cart management.
* Verify expected behaviour for positive and negative inputs.
* Identify, document, and report reproducible defects.

---

## 4. Application Under Test

* **Application:** Swag Labs
* **URL:** https://www.saucedemo.com/


---

## 5. Scope of Testing

### In Scope

* **Authentication**
  * Login page loads correctly.
  * Login with valid and invalid credentials.
  * Empty username and password validation.
  * Appropriate error messages for rejected login attempts.
* **Product Listing**
  * Product inventory page loads after successful login.
  * Product names, descriptions, images, and prices are displayed.
  * Product detail pages open correctly.
  * Product sorting works, if available.
* **Shopping Cart**
  * Add a product to the cart.
  * Verify the cart badge/count, if displayed.
  * Open the cart and verify selected products.
  * Remove a product from the cart.
  * Verify cart state after adding or removing items.
* **Checkout — Initial Coverage**
  * Checkout page opens from the cart.
  * Required customer information is validated.
  * Valid test information allows progression to the next step.
  * Order summary and completion behaviour are checked if time permits.
* **Basic Usability**
  * Important controls and validation messages are visible.
  * Core actions can be completed using a desktop browser.
  * Basic keyboard operation is checked where practical.

### Out of Scope

* Production e-commerce systems or real purchases.
* Payment gateway or financial transaction testing.
* Security penetration testing.
* Load, stress, and performance testing.
* API testing and automated testing during the initial manual phase.
* Exhaustive cross-browser and accessibility certification.

---

## 6. Test Approach

The following techniques will be used:

* Positive testing
* Negative testing
* Equivalence partitioning
* Boundary-value analysis where applicable
* Exploratory testing
* Functional testing
* Basic usability checks
* Retesting and regression checks when a defect or change is identified

---

## 7. Test Environment

| Item | Planned Configuration |
| :--- | :--- |
| **Application** | Public Sauce Demo website |
| **Operating System** | Windows — Version 11 |
| **Browser** | Google Chrome — Version 155 |
| **Viewport** | Desktop; mobile-sized viewport; Tablet |
| **Test Type** | Manual web testing |
| **Documentation** | Markdown files in GitHub |
| **Evidence** | Screenshots with sensitive information excluded |

---

## 8. Test Data

* Use only the public demo credentials documented on the application or in trusted demo documentation.
* Commonly documented standard-user credentials are `standard_user` / `secret_sauce`; confirm that they remain valid before testing.
* Use synthetic customer information for checkout, for example:
  * **First name:** Test
  * **Last name:** User
  * **Postal code:** 12345

---

## 9. Entry Criteria

Testing can begin when:

- [ ] The application is accessible.
- [ ] A suitable browser is available.
- [ ] The required demo account can be accessed, if login is required.
- [ ] The test plan and initial scenarios have been reviewed.
- [ ] The test environment and data have been recorded.

---

## 10. Exit Criteria

The initial test cycle can be considered complete when:

- [ ] All planned in-scope test cases have been executed or marked as blocked/not run with an explanation.
- [ ] Actual results and statuses are recorded.
- [ ] Failures have supporting evidence where practical.
- [ ] Reproducible defects are documented.
- [ ] A test execution summary is prepared.

---

## 11. Defect Reporting

Each reproducible defect should include:

1. **Defect ID**
2. **Short, descriptive title**
3. **Environment**
4. **Preconditions and test data**
5. **Steps to reproduce**
6. **Expected result**
7. **Actual result**
8. **Severity and priority, with rationale**
9. **Screenshot or other supporting evidence**
10. **Current status**

---

## 12. Risks and Mitigations

| Risk | Mitigation |
| :--- | :--- |
| **Public demo is unavailable** | Record the issue and retry later |
| **Demo data or behaviour changes** | Record the date and environment of execution |
| **Shared demo state affects testing** | Start with a clean cart/session where possible |
| **Intentional demo defects are present** | Report only observed and reproducible behaviour |
| **Limited study time** | Prioritise login, product listing, and cart workflows |

---

## 13. Deliverables

* Test plan
* Test scenarios
* Detailed test cases
* Test execution log
* Defect reports, if defects are found
* Evidence folder
* Final test summary

---

## 14. Limitations

This is an independent learning and portfolio project using a public demo application. It is not an official Sauce Labs test report. Features and behaviour must be confirmed during execution, and results must reflect what was actually observed.

---

## 15. Review and Approval

* **Prepared by:** [Mashiat Anjum Talukder]
* **Review status:** Pending
* **Approval status:** Not applicable — independent portfolio projec
