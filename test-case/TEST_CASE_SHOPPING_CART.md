
## Shopping Cart Module

### Module Information

| Field | Details |
|---|---|
| Module Name | Shopping Cart |
| Module ID | `CART` |
| Application | Swag Labs |
| Base URL | https://www.saucedemo.com/ |
| Test Type | Functional and UI Testing |
| Test Cases Document ID | `SL-TC-001` |
| Test Case Status | Not Run |

### Test Data

| Test Data ID | Test Data | Purpose |
|---|---|---|
| TD-CART-001 | `standard_user` / `secret_sauce` | Access the inventory and cart pages |
| TD-CART-002 | Sauce Labs Backpack — $29.99 | Verify adding and removing one product |
| TD-CART-003 | Sauce Labs Bike Light — $9.99 | Verify adding multiple distinct products |
| TD-CART-004 | Sauce Labs Bolt T-Shirt — $15.99 | Verify cart contents and price |
| TD-CART-005 | No products selected | Verify empty cart state |

**Preconditions:** The application is accessible, and the user can log in using `standard_user` / `secret_sauce`. Unless otherwise specified, start each test with an empty cart to avoid interference from previous tests.

---

### TC-CART-001: Verify Cart Badge Count After Adding One Product

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CART-001` |
| Scenario ID | `SL-TS-CART-001` |
| Test Case Title | Verify cart badge count after adding a single product |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in, the inventory page is displayed, and the cart is empty. |
| Test Data | Sauce Labs Backpack — $29.99 |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Verify that the cart badge is not displayed when the cart is empty.
3. Locate the Sauce Labs Backpack product card.
4. Click its **Add to cart** button.
5. Observe the cart icon in the header.
6. Verify the displayed cart badge count.

**Expected Result**

- The product is added to the cart successfully.
- The button changes from **Add to cart** to **Remove**.
- The cart badge displays `1`.
- No unexpected error message is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CART-002: Verify Cart Badge Count After Adding Multiple Distinct Products

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CART-002` |
| Scenario ID | `SL-TS-CART-002` |
| Test Case Title | Verify cart badge count after adding multiple distinct products |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in, the inventory page is displayed, and the cart is empty. |
| Test Data | Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Verify that the cart is initially empty.
3. Click **Add to cart** for Sauce Labs Backpack.
4. Verify that the cart badge displays `1`.
5. Click **Add to cart** for Sauce Labs Bike Light.
6. Verify that the cart badge displays `2`.
7. Click **Add to cart** for Sauce Labs Bolt T-Shirt.
8. Verify that the cart badge displays `3`.
9. Open the shopping cart.
10. Verify that all three selected products are displayed.

**Expected Result**

- Each distinct product is added successfully.
- The cart badge increases by one for each added product.
- The final cart badge count is `3`.
- All three selected products appear in the cart.
- No product is unintentionally duplicated or missing.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CART-003: Verify Cart Badge Count After Removing a Product From the Inventory Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CART-003` |
| Scenario ID | `SL-TS-CART-003` |
| Test Case Title | Verify cart badge count after removing a product from inventory |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in, the inventory page is displayed, and at least two distinct products have been added to the cart. |
| Test Data | Sauce Labs Backpack and Sauce Labs Bike Light |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Add Sauce Labs Bike Light to the cart.
4. Verify that the cart badge displays `2`.
5. Locate the Sauce Labs Backpack product card.
6. Click its **Remove** button.
7. Observe the cart badge.
8. Verify that the badge count decreases by one.
9. Open the shopping cart.
10. Verify that Sauce Labs Backpack is absent and Sauce Labs Bike Light remains.

**Expected Result**

- The selected product is removed from the cart.
- The product button changes from **Remove** to **Add to cart**.
- The cart badge decreases from `2` to `1`.
- The removed product is no longer displayed in the cart.
- The remaining product is preserved.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CART-004: Verify Selected Products, Quantities, and Prices in the Cart

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CART-004` |
| Scenario ID | `SL-TS-CART-004` |
| Test Case Title | Verify selected product information in the shopping cart |
| Priority | High |
| Test Type | Functional and UI |
| Preconditions | The user is logged in and the inventory page is displayed. |
| Test Data | Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Add Sauce Labs Bike Light to the cart.
4. Add Sauce Labs Bolt T-Shirt to the cart.
5. Click the shopping cart icon.
6. Verify that the cart page is displayed.
7. Verify that all three selected products appear in the cart.
8. Compare each displayed product name with the selected product.
9. Verify the displayed price of each product.
10. Verify the quantity shown for each cart item.
11. Confirm that no unselected product is displayed.

**Expected Result**

- The shopping cart page loads successfully.
- All selected products appear with the correct names and prices.
- The expected products and prices are:

| Product Name | Expected Price | Expected Quantity |
|---|---:|---:|
| Sauce Labs Backpack | $29.99 | 1 |
| Sauce Labs Bike Light | $9.99 | 1 |
| Sauce Labs Bolt T-Shirt | $15.99 | 1 |

- The cart contains exactly three distinct products.
- Each product quantity is `1`.
- No unselected or duplicate product appears.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CART-005: Verify Removing a Product From the Shopping Cart Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CART-005` |
| Scenario ID | `SL-TS-CART-005` |
| Test Case Title | Verify product removal from the shopping cart page |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in and at least two distinct products have been added to the cart. |
| Test Data | Sauce Labs Backpack and Sauce Labs Bike Light |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Add Sauce Labs Bike Light to the cart.
4. Open the shopping cart page.
5. Verify that both products are displayed.
6. Locate Sauce Labs Backpack in the cart.
7. Click its **Remove** button.
8. Verify that Sauce Labs Backpack is removed from the cart page.
9. Verify that Sauce Labs Bike Light remains displayed.
10. Observe the cart badge count.

**Expected Result**

- Sauce Labs Backpack is removed successfully from the cart.
- Sauce Labs Bike Light remains in the cart.
- The cart badge decreases from `2` to `1`.
- The remaining cart contents are correct.
- No unexpected error message is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CART-006: Verify Cart Badge and Cart Contents Remain Consistent

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CART-006` |
| Scenario ID | `SL-TS-CART-006` |
| Test Case Title | Verify consistency between cart badge and cart contents |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in and the inventory page is displayed with an empty cart. |
| Test Data | Sauce Labs Backpack, Sauce Labs Bike Light, and Sauce Labs Bolt T-Shirt |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Verify that the cart is initially empty.
3. Add Sauce Labs Backpack to the cart.
4. Add Sauce Labs Bike Light to the cart.
5. Add Sauce Labs Bolt T-Shirt to the cart.
6. Verify that the cart badge displays `3`.
7. Open the shopping cart.
8. Count the displayed cart items and verify that there are three.
9. Remove Sauce Labs Bike Light from the cart page.
10. Verify that the cart badge displays `2`.
11. Verify that exactly two products remain in the cart.
12. Return to the inventory page.
13. Verify that Sauce Labs Bike Light displays **Add to cart**.
14. Verify that the remaining selected products display **Remove**.
15. Open the shopping cart again and confirm the final contents.

**Expected Result**

- The cart badge count matches the number of distinct products in the cart.
- Adding three distinct products results in a badge count of `3`.
- Removing one product results in a badge count of `2`.
- The removed product is absent from the cart.
- The remaining two products are preserved.
- The inventory button states reflect the current cart contents.
- Cart contents remain consistent when navigating between the inventory and cart pages.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CART-007: Verify the Continue Shopping Button

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CART-007` |
| Scenario ID | `SL-TS-CART-007` |
| Test Case Title | Verify navigation using the Continue Shopping button |
| Priority | Low |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in and the shopping cart page is displayed. |
| Test Data | Sauce Labs Backpack |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the shopping cart page.
4. Verify that Sauce Labs Backpack is displayed.
5. Click the **Continue Shopping** button.
6. Verify that the inventory page is displayed.
7. Verify that the Products heading is visible.
8. Verify that the Sauce Labs Backpack button displays **Remove**.
9. Open the cart again.
10. Verify that Sauce Labs Backpack remains in the cart.

**Expected Result**

- Clicking **Continue Shopping** returns the user to the inventory page.
- The inventory page loads successfully.
- The previously selected product remains in the cart.
- The cart badge remains consistent with the cart contents.
- No unexpected error message is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CART-008: Verify the Empty Shopping Cart State

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CART-008` |
| Scenario ID | `SL-TS-CART-008` |
| Test Case Title | Verify the shopping cart when no products have been added |
| Priority | Medium |
| Test Type | Functional and UI |
| Preconditions | The user is logged in and no products have been added to the cart. |
| Test Data | Empty cart |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Ensure that no products have been added to the cart.
3. Click the shopping cart icon.
4. Verify that the shopping cart page is displayed.
5. Observe the cart item list.
6. Verify whether any product items are displayed.
7. Observe the cart badge in the header.
8. Verify that the page provides the expected navigation controls, including **Continue Shopping**.

**Expected Result**

- The shopping cart page loads successfully.
- No product items are displayed.
- The cart badge is not displayed when the cart is empty.
- The **Continue Shopping** button is available.
- The page remains usable without an error.
- No product is added to the cart automatically.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### Test Execution Summary — Shopping Cart

| Metric | Count |
|---|---:|
| Total Test Cases | 8 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 8 |
| Pass Rate | Not calculated — pending execution |

### Execution Notes

- Execute each test case against the actual Swag Labs application.
- Start with an empty cart for independent test cases unless the preconditions specify otherwise.
- Record actual results only after execution.
- Update the status based on observed results.
- Capture screenshots for failures and unexpected behavior.
- Report reproducible defects and link each defect to its related test case.
- For cart badge validation, compare the badge count with the number of distinct selected products, not the sum of quantities unless quantity controls are explicitly available.
- The empty-cart behavior should be verified in the live application rather than assumed.

