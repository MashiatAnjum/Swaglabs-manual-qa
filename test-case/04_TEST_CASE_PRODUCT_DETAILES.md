

##  Product Details Module

###  Module Information

| Field | Details |
|---|---|
| Module Name | Product Details |
| Module ID | `PDT` |
| Application | Swag Labs |
| Base URL | https://www.saucedemo.com/ |
| Test Type | Functional and UI Testing |
| Test Cases Document ID | `SL-TC-001` |
| Test Case Status | Not Run |

###  Test Data

| Test Data ID | Test Data | Purpose |
|---|---|---|
| TD-PDT-001 | `standard_user` / `secret_sauce` | Access the inventory and product details pages |
| TD-PDT-002 | Sauce Labs Backpack — $29.99 | Verify product details and cart actions |
| TD-PDT-003 | Sauce Labs Bike Light — $9.99 | Verify product navigation and details |
| TD-PDT-004 | Sauce Labs Bolt T-Shirt — $15.99 | Verify product details and cart actions |

**Preconditions:** The application is accessible, and the user can log in using `standard_user` / `secret_sauce`. Start with an empty cart unless a test case specifies otherwise.

---

### TC-PDT-001: Verify Product Details Page Navigation

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-PDT-001` |
| Scenario ID | `SL-TS-PDT-001` |
| Test Case Title | Verify that clicking a product name or image opens the corresponding details page |
| Priority | High |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in and the inventory page is displayed. |
| Test Data | Sauce Labs Backpack |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Locate the Sauce Labs Backpack product card.
3. Note the product name displayed on the inventory page.
4. Click the product name.
5. Verify that the product details page opens.
6. Verify that the details page displays Sauce Labs Backpack.
7. Navigate back to the inventory page using the application's navigation or browser navigation.
8. Locate the Sauce Labs Backpack product image.
9. Click the product image.
10. Verify that the corresponding product details page opens.

**Expected Result**

- Clicking the product name opens its corresponding details page.
- Clicking the product image also opens the corresponding details page.
- The displayed product is the one selected from the inventory page.
- The details page loads without an unexpected error.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-PDT-002: Verify Product Information on the Details Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-PDT-002` |
| Scenario ID | `SL-TS-PDT-002` |
| Test Case Title | Verify product information consistency between inventory and details pages |
| Priority | High |
| Test Type | Functional and UI |
| Preconditions | The user is logged in and the inventory page is displayed. |
| Test Data | Sauce Labs Backpack — $29.99 |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Locate Sauce Labs Backpack on the inventory page.
3. Record its displayed name, description, price, and image.
4. Click the product name or image.
5. Verify that the product details page opens.
6. Compare the product name on the details page with the inventory listing.
7. Compare the product description on the details page with the inventory listing.
8. Compare the displayed price on both pages.
9. Verify that the product image corresponds to the selected product.
10. Check that the product information is readable and properly displayed.

**Expected Result**

- The details page displays the correct product.
- The product name matches the inventory listing.
- The description matches the inventory listing.
- The price matches the inventory listing.
- The image corresponds to the selected product.
- No product information is missing or incorrectly associated.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-PDT-003: Verify Adding a Product to the Cart From the Details Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-PDT-003` |
| Scenario ID | `SL-TS-PDT-003` |
| Test Case Title | Verify that a product can be added to the cart from its details page |
| Priority | Medium |
| Test Type | Functional |
| Preconditions | The user is logged in, the inventory page is displayed, and the cart is empty. |
| Test Data | Sauce Labs Backpack — $29.99 |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Verify that the cart is initially empty.
3. Locate Sauce Labs Backpack on the inventory page.
4. Click its product name or image.
5. Verify that the product details page opens.
6. Click the **Add to cart** button on the details page.
7. Observe the product action button.
8. Observe the cart badge in the header.
9. Open the shopping cart.
10. Verify that Sauce Labs Backpack appears in the cart.

**Expected Result**

- The product can be added to the cart from its details page.
- The action button changes from **Add to cart** to **Remove**.
- The cart badge displays `1`.
- Sauce Labs Backpack appears in the shopping cart with the correct price.
- No unexpected error message is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-PDT-004: Verify Removing a Product From the Cart on the Details Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-PDT-004` |
| Scenario ID | `SL-TS-PDT-004` |
| Test Case Title | Verify that a product can be removed from the cart from its details page |
| Priority | Medium |
| Test Type | Functional |
| Preconditions | The user is logged in and the inventory page is displayed. The selected product has already been added to the cart. |
| Test Data | Sauce Labs Backpack — $29.99 |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart from the inventory page.
3. Verify that the cart badge displays `1`.
4. Click the Sauce Labs Backpack product name or image.
5. Verify that the product details page opens.
6. Verify that the action button displays **Remove**.
7. Click the **Remove** button.
8. Observe the action button and cart badge.
9. Open the shopping cart.
10. Verify that Sauce Labs Backpack is no longer displayed.

**Expected Result**

- The details page displays the selected product.
- The action button displays **Remove** when the product is in the cart.
- Clicking **Remove** removes the product from the cart.
- The action button changes back to **Add to cart**.
- The cart badge is no longer displayed when the cart becomes empty.
- Sauce Labs Backpack is absent from the shopping cart.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-PDT-005: Verify the Back to Products Button

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-PDT-005` |
| Scenario ID | `SL-TS-PDT-005` |
| Test Case Title | Verify navigation from the product details page to the inventory page |
| Priority | Medium |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in and a product details page is displayed. |
| Test Data | Sauce Labs Backpack |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Locate Sauce Labs Backpack on the inventory page.
3. Click its product name or image.
4. Verify that the product details page opens.
5. Locate the **Back to products** button.
6. Click the button.
7. Verify that the inventory page is displayed.
8. Verify that the page heading displays "Products".
9. Verify that the product inventory is visible.
10. Confirm that the user can access the product list again.

**Expected Result**

- Clicking **Back to products** returns the user to the inventory page.
- The inventory page loads successfully.
- The "Products" heading is visible.
- The product inventory is displayed.
- The user can select another product or continue shopping.
- No unexpected error message is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

###  Test Execution Summary — Product Details

| Metric | Count |
|---|---:|
| Total Test Cases | 5 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 5 |
| Pass Rate | Not calculated — pending execution |

###  Execution Notes

- Execute each test case against the actual Swag Labs application.
- Record actual results only after performing the test steps.
- Update each test case status based on observed results.
- Capture screenshots for failures and unexpected behavior.
- Link reproducible defects to their corresponding test case IDs.
- Verify the product information against the inventory listing rather than relying only on memory.
- For cart-related tests, check the product action button, cart badge, and actual cart contents to ensure consistency.
