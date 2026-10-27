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
| **TS_LOG_01** | Verify successful user login using valid credentials (`standard_user`). | High |
| **TS_LOG_02** | Verify user login behavior when using invalid credentials. | High |
| **TS_LOG_03** | Verify system behavior when attempting to log in with empty username or password fields. High |
| **TS_LOG_04** | Verify error message display for locked-out user account (`locked_out_user`).| Medium |
| **TS_LOG_05** | Verify user login behavior under problem user (`problem_user`) and performance glitch user (`performance_glitch_user`). | Medium |

---

### B. Products / Inventory Module (`TS_INV`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_INV_01** | Verify that product catalog properly displays product names, images, descriptions, and prices.| High |
| **TS_INV_02** | Verify product sorting functionality by **Name (A to Z)**. | Medium |
| **TS_INV_03** | Verify product sorting functionality by **Name (Z to A)**.| Medium |
| **TS_INV_04** | Verify product sorting functionality by **Price (low to high)**. | Medium |
| **TS_INV_05** | Verify product sorting functionality by **Price (high to low)**. | Medium |

---

### C. Shopping Cart Module (`TS_CART`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_CART_01** | Verify adding items to the cart updates the cart badge counter correctly. | High |
| **TS_CART_02** | Verify removing items from the cart updates the cart badge counter correctly. | High |
| **TS_CART_03** | Verify product quantities and selected items in the shopping cart list. | High |
| **TS_CART_04** | Verify that clicking "Continue Shopping" redirects back to the inventory page. | Low |

---

### D. Product Details Module (`TS_PDT`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_PDT_01** | Verify clicking on a product name or image redirects to the correct Product Details page. | High |
| **TS_PDT_02** | Verify product information (image, title, description, price) on the details page matches the catalog. | High |
| **TS_PDT_03** | Verify adding and removing products directly from the Product Details page. | Medium |
| **TS_PDT_04** | Verify navigation back to the product catalog using the "Back to products" button.| Medium |

---

### E. Checkout Module (`TS_CHK`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_CHK_01** | Verify entering valid customer information (First Name, Last Name, Zip/Postal Code). | High |
| **TS_CHK_02** | Verify input validation and error messages when leaving required customer fields blank.| High |
| **TS_CHK_03** | Verify clicking the "Cancel" button returns the user back to the Shopping Cart page.| Medium |

---

### F. Order Overview Module (`TS_OOV`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_OOV_01** | Verify that listed items and quantities on the overview page match the selected cart items. | High |
| **TS_OOV_02** | Verify correct calculation of Item Subtotal price. | High |
| **TS_OOV_03** | Verify correct calculation of Tax amount.[cite: 6] | High |
| **TS_OOV_04** | Verify correct calculation of Total price (Subtotal + Tax = Total). High |
| **TS_OOV_05** | Verify clicking "Cancel" on the overview page aborts the order and returns to the catalog.\ | Medium |

---

### G. Order Completion Module (`TS_OCM`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_OCM_01** | Verify successful order placement upon clicking the "Finish" button. | High |
| **TS_OCM_02** | Verify order confirmation header text ("Thank you for your order!"). | Medium |
| **TS_OCM_03** | Verify clicking "Back Home" redirects user back to the inventory page and clears active cart state. | High |

---

### H. Navigation Module (`TS_NAV`)
| Scenario ID | Test Scenario Description | Priority |
| :--- | :--- | :--- |
| **TS_NAV_01** | Verify opening and closing of the hamburger side navigation menu.| Medium |
| **TS_NAV_02** | Verify side menu navigation options ("All Items", "About", "Logout", "Reset App State"). | High |
| **TS_NAV_03** | Verify clicking "Logout" terminates user session and redirects to the login page.| High |
| **TS_NAV_04** | Verify browser back/forward navigation behavior across application steps. | Medium |
