
## Products 

###  Module Information

| Field | Details |
|---|---|
| Module Name | Products / Inventory |
| Module ID | `INV` |
| Application | Swag Labs |
| Base URL | https://www.saucedemo.com/ |
| Test Type | Functional, UI, and Sorting Testing |
| Test Cases Document ID | `SL-TC-001` |
| Test Case Status | Not Run |

###  Test Data

| Test Data ID | Test Data | Purpose |
|---|---|---|
| TD-INV-001 | `standard_user` / `secret_sauce` | Access the inventory page |
| TD-INV-002 | Name (A to Z) | Verify ascending alphabetical sorting |
| TD-INV-003 | Name (Z to A) | Verify descending alphabetical sorting |
| TD-INV-004 | Price (low to high) | Verify ascending price sorting |
| TD-INV-005 | Price (high to low) | Verify descending price sorting |

**Precondition for all test cases:** The application is accessible, the user is logged in successfully using `standard_user`, and the Products / Inventory page is displayed unless otherwise specified.

---

### TC-INV-001: Verify that the Product Inventory Page Loads Successfully

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-INV-001` |
| Scenario ID | `SL-TS-INV-001` |
| Test Case Title | Verify successful loading of the product inventory page |
| Priority | High |
| Test Type | Functional |
| Preconditions | The user is logged in successfully using valid credentials. |
| Test Data | `standard_user` / `secret_sauce` |

**Test Steps**

1. Open https://www.saucedemo.com/ in a supported browser.
2. Enter `standard_user` in the Username field.
3. Enter `secret_sauce` in the Password field.
4. Click the Login button.
5. Observe the page after successful authentication.
6. Verify the page heading, product list, and sorting control.

**Expected Result**

- The user is redirected to the product inventory page.
- The page heading displays "Products".
- Product cards are displayed.
- The sorting dropdown is visible and usable.
- The cart icon is visible in the header.
- No unexpected error message or broken page layout is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-INV-002: Verify Product Names, Images, Descriptions, and Prices

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-INV-002` |
| Scenario ID | `SL-TS-INV-002` |
| Test Case Title | Verify product information and image display |
| Priority | High |
| Test Type | UI and Functional |
| Preconditions | The user is logged in as `standard_user` and the inventory page is displayed. |
| Test Data | All products displayed in the inventory |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Observe all product cards on the inventory page.
3. Verify that each product has a visible name.
4. Verify that each product has a description.
5. Verify that each product has an image.
6. Verify that each product has a displayed price.
7. Compare the product names, images, descriptions, and prices against the expected application data.
8. Scroll through the entire inventory page if necessary.
9. Check for missing information, incorrect product details, broken images, or duplicated product cards.

**Expected Result**

- Every expected product is displayed.
- Product names and descriptions are readable and associated with the correct products.
- Product images load successfully and correspond to the displayed products.
- Prices are visible and use the expected currency and two-decimal format.
- No expected product information is missing or incorrectly associated.

**Reference Product Data**

| Product Name | Expected Price |
|---|---:|
| Sauce Labs Backpack | $29.99 |
| Sauce Labs Bike Light | $9.99 |
| Sauce Labs Bolt T-Shirt | $15.99 |
| Sauce Labs Fleece Jacket | $49.99 |
| Sauce Labs Onesie | $7.99 |
| Test.allTheThings() T-Shirt (Red) | $15.99 |

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-INV-003: Verify Product Sorting by Name in Ascending Order (A to Z)

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-INV-003` |
| Scenario ID | `SL-TS-INV-003` |
| Test Case Title | Verify alphabetical sorting in ascending order |
| Priority | Medium |
| Test Type | Functional |
| Preconditions | The inventory page is displayed and the sorting dropdown is available. |
| Test Data | Name (A to Z) |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Locate the product sorting dropdown.
3. Select "Name (A to Z)".
4. Observe the order of the product names.
5. Compare the displayed sequence with alphabetical ascending order.
6. Verify the position of the first and last products.

**Expected Result**

- The products are sorted alphabetically in ascending order.
- The expected sequence is:

   1. Sauce Labs Backpack
   2. Sauce Labs Bike Light
   3. Sauce Labs Bolt T-Shirt
   4. Sauce Labs Fleece Jacket
   5. Sauce Labs Onesie
   6. Test.allTheThings() T-Shirt (Red)

- No product is missing or duplicated after sorting.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-INV-004: Verify Product Sorting by Name in Descending Order (Z to A)

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-INV-004` |
| Scenario ID | `SL-TS-INV-004` |
| Test Case Title | Verify alphabetical sorting in descending order |
| Priority | Medium |
| Test Type | Functional |
| Preconditions | The inventory page is displayed and the sorting dropdown is available. |
| Test Data | Name (Z to A) |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Locate the product sorting dropdown.
3. Select "Name (Z to A)".
4. Observe the order of the product names.
5. Compare the displayed sequence with alphabetical descending order.
6. Verify the position of the first and last products.

**Expected Result**

- The products are sorted alphabetically in descending order.
- The expected sequence is:

   1. Test.allTheThings() T-Shirt (Red)
   2. Sauce Labs Onesie
   3. Sauce Labs Fleece Jacket
   4. Sauce Labs Bolt T-Shirt
   5. Sauce Labs Bike Light
   6. Sauce Labs Backpack

- No product is missing or duplicated after sorting.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-INV-005: Verify Product Sorting by Price in Ascending Order (Low to High)

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-INV-005` |
| Scenario ID | `SL-TS-INV-005` |
| Test Case Title | Verify product price sorting in ascending order |
| Priority | Medium |
| Test Type | Functional |
| Preconditions | The inventory page is displayed and product prices are visible. |
| Test Data | Price (low to high) |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Locate the product sorting dropdown.
3. Select "Price (low to high)".
4. Observe the displayed product prices.
5. Compare the sequence of prices with ascending numerical order.
6. Verify that the lowest-priced product appears first.
7. Verify that the highest-priced product appears last.
8. Confirm that products with equal prices are both displayed.

**Expected Result**

- Products are sorted by price from lowest to highest.
- The expected price sequence is:

   1. Sauce Labs Onesie — $7.99
   2. Sauce Labs Bike Light — $9.99
   3. Sauce Labs Bolt T-Shirt — $15.99
   4. Test.allTheThings() T-Shirt (Red) — $15.99
   5. Sauce Labs Backpack — $29.99
   6. Sauce Labs Fleece Jacket — $49.99

- Products with equal prices remain present.
- No product is missing or duplicated.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-INV-006: Verify Product Sorting by Price in Descending Order (High to Low)

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-INV-006` |
| Scenario ID | `SL-TS-INV-006` |
| Test Case Title | Verify product price sorting in descending order |
| Priority | Medium |
| Test Type | Functional |
| Preconditions | The inventory page is displayed and product prices are visible. |
| Test Data | Price (high to low) |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Locate the product sorting dropdown.
3. Select "Price (high to low)".
4. Observe the displayed product prices.
5. Compare the sequence of prices with descending numerical order.
6. Verify that the highest-priced product appears first.
7. Verify that the lowest-priced product appears last.
8. Confirm that products with equal prices are both displayed.

**Expected Result**

- Products are sorted by price from highest to lowest.
- The expected price sequence is:

   1. Sauce Labs Fleece Jacket — $49.99
   2. Sauce Labs Backpack — $29.99
   3. Sauce Labs Bolt T-Shirt — $15.99
   4. Test.allTheThings() T-Shirt (Red) — $15.99
   5. Sauce Labs Bike Light — $9.99
   6. Sauce Labs Onesie — $7.99

- Products with equal prices remain present.
- No product is missing or duplicated.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-INV-007: Verify the Selected Sorting Option Is Reflected in the Product Order

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-INV-007` |
| Scenario ID | `SL-TS-INV-007` |
| Test Case Title | Verify sorting selection and displayed product order remain consistent |
| Priority | Medium |
| Test Type | Functional and UI |
| Preconditions | The inventory page is displayed and the sorting dropdown is available. |
| Test Data | All four sorting options |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Select "Name (A to Z)" from the sorting dropdown.
3. Verify that the selected option is displayed in the dropdown.
4. Verify that the product names follow ascending alphabetical order.
5. Select "Name (Z to A)".
6. Verify that the selected option is displayed and the product order changes accordingly.
7. Select "Price (low to high)".
8. Verify that the selected option is displayed and the product prices follow ascending order.
9. Select "Price (high to low)".
10. Verify that the selected option is displayed and the product prices follow descending order.
11. Confirm that each selection updates the product order without requiring a page reload.
12. Verify that all expected products remain displayed after each sorting operation.

**Expected Result**

- The dropdown reflects the currently selected sorting option.
- The displayed product order matches the selected sorting rule.
- Changing the sorting option updates the product order correctly.
- All expected products remain visible in the inventory.
- No unexpected page reload, error, missing product, or duplicate product occurs.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

###  Test Execution Summary — Products / Inventory

| Metric | Count |
|---|---:|
| Total Test Cases | 7 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 7 |
| Pass Rate | Not calculated — pending execution |

###  Execution Notes

- Execute each test case against the actual Swag Labs application.
- Record the actual result only after performing the test steps.
- Update the status to Passed, Failed, or Blocked based on the observed result.
- Capture screenshots for failures and unexpected behavior.
- If a defect is found, record a reproducible bug report and link it to the relevant test case.
- For products with equal prices, verify the numerical sorting order and the presence of both products. Do not report a defect solely because two equally priced products appear in a different relative order unless a specific ordering requirement exists.
- Record the browser and operating system versions in the main test environment section of this document.

