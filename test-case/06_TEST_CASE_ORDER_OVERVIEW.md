
## Order Overview Module

### Module Information

| Field | Details |
|---|---|
| Module Name | Order Overview |
| Module ID | `OOV` |
| Application | Swag Labs |
| Base URL | https://www.saucedemo.com/ |
| Test Type | Functional, UI, and Calculation Testing |
| Test Cases Document ID | `SL-TC-001` |
| Test Case Status | Not Run |

### Test Data

| Test Data ID | Test Data | Purpose |
|---|---|---|
| TD-OOV-001 | `standard_user` / `secret_sauce` | Access the application |
| TD-OOV-002 | Sauce Labs Backpack — $29.99 | Verify a single product in the overview |
| TD-OOV-003 | Sauce Labs Bike Light — $9.99 | Verify multiple products and calculations |
| TD-OOV-004 | Sauce Labs Bolt T-Shirt — $15.99 | Verify product information and subtotal |
| TD-OOV-005 | Subtotal, tax, and total displayed by the application | Verify order calculations |

**Preconditions:** The application is accessible, and the user can log in using `standard_user` / `secret_sauce`. Products must be added to the cart before checkout. Valid customer information must be submitted to access the Order Overview page.

---

### TC-OOV-001: Verify Selected Products and Quantities on the Order Overview Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OOV-001` |
| Scenario ID | `SL-TS-OOV-001` |
| Test Case Title | Verify that the Order Overview displays the same products and quantities as the shopping cart |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in and the cart contains the selected products. |
| Test Data | Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Add Sauce Labs Bike Light to the cart.
4. Add Sauce Labs Bolt T-Shirt to the cart.
5. Open the shopping cart.
6. Verify that all three selected products are displayed.
7. Click **Checkout**.
8. Enter valid First Name, Last Name, and ZIP/Postal Code information.
9. Click **Continue**.
10. Verify that the Order Overview page is displayed.
11. Compare the product names on the overview page with those in the shopping cart.
12. Verify the quantity displayed for each product.
13. Confirm that no selected product is missing and no unexpected product is included.

**Expected Result**

- The Order Overview page loads successfully.
- All three selected products appear on the overview page.
- Product names match the shopping cart.
- Each selected product has the expected quantity of `1`.
- No product is missing, duplicated, or unexpectedly added.
- The order contents are consistent with the shopping cart.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OOV-002: Verify Product Names and Individual Prices on the Order Overview Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OOV-002` |
| Scenario ID | `SL-TS-OOV-002` |
| Test Case Title | Verify product names and individual prices on the Order Overview page |
| Priority | High |
| Test Type | Functional and UI |
| Preconditions | The user is logged in, the selected products are in the cart, and the Order Overview page is accessible. |
| Test Data | Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Add Sauce Labs Bike Light to the cart.
4. Add Sauce Labs Bolt T-Shirt to the cart.
5. Open the shopping cart and verify the selected products.
6. Click **Checkout**.
7. Enter valid customer information and click **Continue**.
8. Locate each product on the Order Overview page.
9. Compare each displayed product name with the shopping cart and inventory listing.
10. Compare the individual price of each product with the expected price.
11. Verify that each price is associated with the correct product.

**Expected Result**

- All selected products are displayed with the correct names.
- Individual product prices match the inventory listing.
- The expected product data is:

| Product Name | Expected Price |
|---|---:|
| Sauce Labs Backpack | $29.99 |
| Sauce Labs Bike Light | $9.99 |
| Sauce Labs Bolt T-Shirt | $15.99 |

- Prices are displayed in the expected currency and format.
- No price is missing or associated with the wrong product.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OOV-003: Verify Correct Calculation of the Item Subtotal

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OOV-003` |
| Scenario ID | `SL-TS-OOV-003` |
| Test Case Title | Verify that the item subtotal is calculated correctly |
| Priority | High |
| Test Type | Calculation and Functional |
| Preconditions | The user is logged in, and the Order Overview page is displayed with the selected products. |
| Test Data | Sauce Labs Backpack ($29.99), Sauce Labs Bike Light ($9.99), and Sauce Labs Bolt T-Shirt ($15.99) |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Add Sauce Labs Bike Light to the cart.
4. Add Sauce Labs Bolt T-Shirt to the cart.
5. Open the shopping cart.
6. Verify that all three products are present.
7. Click **Checkout**.
8. Enter valid customer information and click **Continue**.
9. Verify the individual product prices on the Order Overview page.
10. Calculate the expected subtotal by adding the individual prices.
11. Compare the calculated subtotal with the displayed Item total.

**Expected Result**

- The subtotal is calculated using the prices of all selected products.
- The expected calculation is:

  `$29.99 + $9.99 + $15.99 = $55.97`

- The displayed Item total is `$55.97`.
- Tax and other totals are not included in the item subtotal.
- No selected product price is omitted or counted more than once.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OOV-004: Verify Correct Calculation of Tax

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OOV-004` |
| Scenario ID | `SL-TS-OOV-004` |
| Test Case Title | Verify that the tax amount is calculated correctly |
| Priority | High |
| Test Type | Calculation and Functional |
| Preconditions | The user is logged in, and the Order Overview page displays the selected products, subtotal, and tax. |
| Test Data | Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt to the cart.
3. Open the cart and click **Checkout**.
4. Enter valid customer information and click **Continue**.
5. Verify that the Order Overview page is displayed.
6. Record the displayed Item total.
7. Record the displayed tax amount.
8. Calculate the expected tax using the application's applicable tax rule.
9. Compare the calculated tax with the displayed tax amount.
10. Verify that the tax is not mistakenly calculated using the final total instead of the item subtotal.

**Expected Result**

- The tax amount is displayed on the Order Overview page.
- Tax is calculated according to the application's pricing rules.
- The calculated tax matches the displayed tax, allowing for the application's currency rounding.
- The tax calculation uses the correct item subtotal.
- No unexpected or duplicate tax amount is included.

**Reference Calculation**

For the standard Swag Labs demo, the tax is typically 8% of the item subtotal.

`$55.97 × 8% = $4.4776`

Rounded to two decimal places, the expected tax is `$4.48`.

Verify the actual displayed tax rule during execution before recording the test result.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OOV-005: Verify the Final Total Equals the Subtotal Plus Tax

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OOV-005` |
| Scenario ID | `SL-TS-OOV-005` |
| Test Case Title | Verify that the final order total equals the item subtotal plus tax |
| Priority | High |
| Test Type | Calculation and Functional |
| Preconditions | The user is logged in, and the Order Overview page displays the item subtotal, tax, and total. |
| Test Data | Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt to the cart.
3. Open the cart and click **Checkout**.
4. Enter valid customer information and click **Continue**.
5. Verify that the Order Overview page is displayed.
6. Record the displayed Item total.
7. Record the displayed Tax amount.
8. Record the displayed Total amount.
9. Calculate the expected final total by adding the item subtotal and tax.
10. Compare the calculated total with the displayed Total amount.

**Expected Result**

- The item subtotal, tax, and final total are displayed.
- The final total equals the item subtotal plus tax.
- Using the reference values, the expected calculation is:

  `Item total + Tax = Total`

  `$55.97 + $4.48 = $60.45`

- The displayed Total is `$60.45`, assuming the standard 8% demo tax rule.
- All monetary calculations are consistent to two decimal places.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-OOV-006: Verify the Cancel Button on the Order Overview Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-OOV-006` |
| Scenario ID | `SL-TS-OOV-006` |
| Test Case Title | Verify that Cancel aborts checkout and returns the user to the inventory page |
| Priority | Medium |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in, at least one product is in the cart, and the Order Overview page is displayed. |
| Test Data | Sauce Labs Backpack — $29.99 |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the shopping cart.
4. Click **Checkout**.
5. Enter valid customer information.
6. Click **Continue**.
7. Verify that the Order Overview page is displayed.
8. Locate the **Cancel** button.
9. Click **Cancel**.
10. Observe the page displayed after clicking Cancel.
11. Verify that the inventory page is displayed.
12. Verify that the Products heading is visible.
13. Check the cart badge and confirm that the selected product remains in the cart.

**Expected Result**

- Clicking **Cancel** aborts the checkout flow.
- The user returns to the inventory page.
- The Products heading and inventory list are displayed.
- The order is not completed.
- The previously selected product remains in the cart unless the application demonstrates otherwise.
- The cart badge remains consistent with the cart contents.
- No order confirmation message is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### Test Execution Summary — Order Overview

| Metric | Count |
|---|---:|
| Total Test Cases | 6 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 6 |
| Pass Rate | Not calculated — pending execution |

###  Execution Notes

- Execute all test cases against the actual Swag Labs application.
- Record actual results only after performing the test steps.
- Update each test case status based on the observed result.
- Capture screenshots of the Order Overview page for calculation checks.
- Compare product information against the inventory and shopping cart.
- Use the actual displayed tax rule when validating the tax amount.
- Record any difference between the calculated and displayed totals.
- Report reproducible defects and link them to the corresponding test case ID.
- Do not change the expected result merely to match an unexpected application result.

