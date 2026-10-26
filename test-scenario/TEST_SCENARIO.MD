# Swag Labs - Test Scenario Document

**Project Name:** Swag Labs E-Commerce Manual Testing  
**Application:** [https://www.saucedemo.com/](https://www.saucedemo.com/)  
**Prepared By:** [Mashiat Anjum Talukder]  
**Date:** October 26, 2026  

---

## 1. Introduction
This document outlines the high-level **Test Scenarios** for testing the Swag Labs e-commerce application. The test scenarios cover key user journeys, including user authentication, product catalog management, shopping cart operations, and the checkout workflow.

---

## 2. Test Scenarios by Module

### A. Login Module (`TS_LOG`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_LOG_01** | Verify successful user login using valid standard credentials (`standard_user`).[cite: 1] | High |
| **TS_LOG_02** | Verify login behavior when using a locked-out user account (`locked_out_user`).[cite: 1] | High |
| **TS_LOG_03** | Verify login behavior when using a problem user account (`problem_user`).[cite: 1] | Medium |
| **TS_LOG_04** | Verify login behavior when using a performance glitch user (`performance_glitch_user`).[cite: 1] | Medium |
| **TS_LOG_05** | Verify error handling when logging in with invalid username or password. | High |
| **TS_LOG_06** | Verify inline error validation when attempting to log in with blank fields. | Medium |

---

### B. Inventory / Product Catalog Module (`TS_INV`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_INV_01** | Verify that the product catalog displays item images, names, descriptions, prices, and "Add to cart" buttons correctly.[cite: 2] | High |
| **TS_INV_02** | Verify product sorting functionality by **Name (A to Z)**.[cite: 2] | Medium |
| **TS_INV_03** | Verify product sorting functionality by **Name (Z to A)**. | Medium |
| **TS_INV_04** | Verify product sorting functionality by **Price (low to high)**. | Medium |
| **TS_INV_05** | Verify product sorting functionality by **Price (high to low)**. | Medium |
| **TS_INV_06** | Verify clicking on a product name/image redirects the user to the product details page. | Medium |

---

### C. Shopping Cart Module (`TS_CART`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_CART_01** | Verify that clicking "Add to cart" on a product updates the shopping cart badge count accurately.[cite: 4] | High |
| **TS_CART_02** | Verify that products added from the inventory page are displayed correctly in the Cart page with proper quantity, description, and price.[cite: 4] | High |
| **TS_CART_03** | Verify the "Remove" button functionality on the Cart page (removes item and updates badge count).[cite: 4] | High |
| **TS_CART_04** | Verify that clicking "Continue Shopping" redirects the user back to the inventory page.[cite: 4] | Low |

---

### D. Checkout Workflow (`TS_CHK`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_CHK_01** | Verify form validation and error messages when required fields (First Name, Last Name, Zip/Postal Code) are left blank during checkout info entry.[cite: 5] | High |
| **TS_CHK_02** | Verify successful progression to the checkout overview page after filling out valid customer information.[cite: 5] | High |
| **TS_CHK_03** | Verify order summary calculations on the checkout overview page (Item total + Tax = Total amount). | High |
| **TS_CHK_04** | Verify successful order completion and confirmation message display after clicking "Finish". | High |

---

### E. Navigation & Session Module (`TS_NAV`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_NAV_01** | Verify all options inside the hamburger menu ("All Items", "About", "Logout", "Reset App State").[cite: 3] | High |
| **TS_NAV_02** | Verify user session termination and redirection back to the login page upon clicking "Logout".[cite: 1, 3] | High |
| **TS_NAV_03** | Verify "Reset App State" functionality clears cart items and resets inventory buttons.[cite: 2, 3] | Medium |
