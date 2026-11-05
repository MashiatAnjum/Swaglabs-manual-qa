
# Order Completion Module

## Module Information

| Field | Details |
|---|---|
| Module Name | Order Completion |
| Module ID | `OCM` |
| Application | Swag Labs |
| Base URL | https://www.saucedemo.com/ |
| Test Type | Functional, UI, and Navigation Testing |
| Test Cases Document ID | `SL-TC-001` |
| Test Case Status | Not Run |

### Test Data

| Test Data ID | Test Data | Purpose |
|---|---|---|
| TD-OCM-001 | `standard_user` / `secret_sauce` | Access the application |
| TD-OCM-002 | Sauce Labs Backpack — $29.99 | Verify successful order completion with a single product |
| TD-OCM-003 | First Name: Mashiat; Last Name: Talukder; ZIP Code: 1212 | Provide valid customer information during checkout |
| TD-OCM-004 | `Thank you for your order!` | Verify the order confirmation header |
| TD-OCM-005 | `Your order has been dispatched, and will arrive just as fast as the pony can get there!` | Verify the order confirmation message |
| TD-OCM-006 | Back Home button | Verify navigation to the Inventory page |
| TD-OCM-007 | Sauce Labs Backpack and Sauce Labs Bike Light | Verify cart state after successful order completion |

**Preconditions:** The application is accessible, and the user can log in using `standard_user` / `secret_sauce`. Products must be added to the cart before checkout. Valid customer information must be submitted to access the Order Overview page.

---

### TC-OCM-001: Complete Order Successfully

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OCM-001` |
| Scenario ID | `SL-TS-OCM-001` |
| Test Case Title | Verify that clicking the Finish button completes the order successfully |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in as `standard_user`, has added at least one product to the cart, and has proceeded through checkout to the Order Overview page with valid customer information. |
| Test Data | Sauce Labs Backpack; First Name: Mashiat; Last Name: Talukder; ZIP Code: 1212 |

**Test Steps**

1. Log in to the application using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the shopping cart.
4. Click **Checkout**.
5. Enter valid First Name, Last Name, and ZIP/Postal Code information.
6. Click **Continue**.
7. Verify that the Order Overview page is displayed.
8. Click the **Finish** button.
9. Observe the page displayed after clicking Finish.

**Expected Result**

- The order is completed successfully.
- The user is redirected to the Order Completion page.
- The page displays the order confirmation content.
- No error message is displayed during successful order completion.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OCM-002: Verify Order Confirmation Header

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OCM-002` |
| Scenario ID | `SL-TS-OCM-002` |
| Test Case Title | Verify the order confirmation header |
| Priority | High |
| Test Type | UI and Functional |
| Preconditions | The user is logged in, has added at least one product to the cart, completed checkout with valid customer information, and reached the Order Overview page. |
| Test Data | Expected header: `Thank you for your order!` |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add at least one product to the cart.
3. Open the shopping cart.
4. Click **Checkout**.
5. Enter valid customer information.
6. Click **Continue**.
7. Verify that the Order Overview page is displayed.
8. Click **Finish**.
9. Locate the order confirmation header.
10. Verify the displayed text against the expected header.

**Expected Result**

- The Order Completion page is displayed successfully.
- The confirmation header reads exactly **"Thank you for your order!"**.
- The confirmation header is clearly visible to the user.
- No spelling or text mismatch is observed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OCM-003: Verify Order Confirmation Message

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OCM-003` |
| Scenario ID | `SL-TS-OCM-003` |
| Test Case Title | Verify the order confirmation message |
| Priority | Medium |
| Test Type | Functional and UI |
| Preconditions | The user is logged in, has added at least one product to the cart, completed checkout with valid customer information, and reached the Order Overview page. |
| Test Data | Expected message: `Your order has been dispatched, and will arrive just as fast as the pony can get there!` |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add at least one product to the cart.
3. Open the shopping cart.
4. Click **Checkout**.
5. Enter valid customer information.
6. Click **Continue**.
7. Verify that the Order Overview page is displayed.
8. Click **Finish**.
9. Locate the order confirmation message beneath the confirmation header.
10. Verify the displayed message against the expected text.

**Expected Result**

- The Order Completion page is displayed successfully.
- The order confirmation message is displayed beneath the confirmation header.
- The message matches the expected text exactly.
- The message is readable and clearly visible on the page.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OCM-004: Verify Back Home Navigation

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OCM-004` |
| Scenario ID | `SL-TS-OCM-004` |
| Test Case Title | Verify that the Back Home button redirects the user to the Inventory page |
| Priority | High |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in, has added at least one product to the cart, completed checkout with valid customer information, and is on the Order Overview page. |
| Test Data | Button: `Back Home`; Expected destination: Inventory page |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add at least one product to the cart.
3. Open the shopping cart.
4. Click **Checkout**.
5. Enter valid customer information.
6. Click **Continue**.
7. Verify that the Order Overview page is displayed.
8. Click **Finish**.
9. Verify that the Order Completion page is displayed.
10. Locate and click the **Back Home** button.
11. Observe the destination page.
12. Verify that the Inventory page is displayed.
13. Verify that the Products heading and product listing are visible.
14. Check whether the available inventory controls are accessible.

**Expected Result**

- Clicking **Back Home** redirects the user to the Inventory page.
- The Products heading is displayed.
- The product listing is displayed successfully.
- The user can interact with the available inventory controls.
- No unexpected error or broken page is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OCM-005: Verify Cart State After Order Completion

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OCM-005` |
| Scenario ID | `SL-TS-OCM-005` |
| Test Case Title | Verify that the cart badge and active cart state are cleared after successful order completion |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in and has added one or more products to the cart before proceeding through checkout to the Order Overview page. |
| Test Data | Sauce Labs Backpack — $29.99; Sauce Labs Bike Light — $9.99 |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Add Sauce Labs Bike Light to the cart.
4. Open the shopping cart.
5. Verify that both selected products are displayed.
6. Click **Checkout**.
7. Enter valid First Name, Last Name, and ZIP/Postal Code information.
8. Click **Continue**.
9. Verify that the Order Overview page is displayed.
10. Click **Finish**.
11. Verify that the Order Completion page is displayed.
12. Click **Back Home** to return to the Inventory page.
13. Inspect the shopping cart badge.
14. Verify whether the cart badge is displayed.
15. Open the shopping cart.
16. Verify that the previously purchased products are no longer present in the active cart.

**Expected Result**

- The order is completed successfully.
- The user is redirected to the Inventory page after clicking **Back Home**.
- The cart badge is no longer displayed when the cart is empty.
- The previously purchased products are no longer present in the active cart.
- The shopping cart displays an empty state.
- The cart contents reflect the cleared state after successful order completion.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### Test Execution Summary — Order Completion

| Metric | Count |
|---|---:|
| Total Test Cases | 5 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 5 |
| Pass Rate | Not calculated — pending execution |

### Execution Notes

- Execute all test cases against the actual Swag Labs application.
- Complete the checkout process before executing the Order Completion test cases.
- Record actual results only after performing the test steps.
- Update each test case status based on the observed result.
- Capture screenshots of the Order Completion page as evidence.
- Verify the confirmation header and message against the expected text.
- Verify that the Back Home button redirects the user to the Inventory page.
- Check the cart badge and cart contents after successful order completion.
- Report reproducible defects and link them to the corresponding test case ID.
- Do not change the expected result merely to match an unexpected application result.
