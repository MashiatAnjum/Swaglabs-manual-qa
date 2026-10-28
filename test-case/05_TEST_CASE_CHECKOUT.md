
## Checkout Module

###  Module Information

| Field | Details |
|---|---|
| Module Name | Checkout |
| Module ID | `CHK` |
| Application | Swag Labs |
| Base URL | https://www.saucedemo.com/ |
| Test Type | Functional and Validation Testing |
| Test Cases Document ID | `SL-TC-001` |
| Test Case Status | Not Run |

###  Test Data

| Test Data ID | Test Data | Purpose |
|---|---|---|
| TD-CHK-001 | `standard_user` / `secret_sauce` | Log in to the application |
| TD-CHK-002 | First Name: `Mashiat`; Last Name: `Talukder`; ZIP Code: `1212` | Valid customer information |
| TD-CHK-003 | All fields empty | Validate all required fields |
| TD-CHK-004 | First Name empty; Last Name: `Talukder`; ZIP Code: `1212` | Validate first name |
| TD-CHK-005 | First Name: `Mashiat`; Last Name empty; ZIP Code: `1212` | Validate last name |
| TD-CHK-006 | First Name: `Mashiat`; Last Name: `Talukder`; ZIP Code empty | Validate ZIP/postal code |
| TD-CHK-007 | Sauce Labs Backpack — $29.99 | Cart item for checkout testing |
| TD-CHK-008 | Empty cart | Observe checkout behavior with no products |

**Preconditions:** The application is accessible, and the user can log in using `standard_user` / `secret_sauce`. For test cases requiring a product, add Sauce Labs Backpack to the cart before proceeding.

---

### TC-CHK-001: Verify Checkout Button Navigation

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CHK-001` |
| Scenario ID | `SL-TS-CHK-001` |
| Test Case Title | Verify that the Checkout button opens the customer information page |
| Priority | High |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in and at least one product has been added to the cart. |
| Test Data | Sauce Labs Backpack — $29.99 |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Click the shopping cart icon.
4. Verify that the cart page is displayed.
5. Verify that Sauce Labs Backpack appears in the cart.
6. Click the **Checkout** button.
7. Observe the page displayed after clicking Checkout.
8. Verify that the customer information form is displayed.

**Expected Result**

- The cart page opens successfully.
- The selected product is displayed in the cart.
- Clicking **Checkout** opens the customer information page.
- The First Name, Last Name, and ZIP/Postal Code fields are visible.
- The Continue and Cancel buttons are displayed.
- No unexpected error message is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CHK-002: Verify Checkout With Valid Customer Information

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CHK-002` |
| Scenario ID | `SL-TS-CHK-002` |
| Test Case Title | Verify that valid customer information allows progression to Order Overview |
| Priority | High |
| Test Type | Functional and Validation |
| Preconditions | The user is logged in, a product is in the cart, and the customer information page is accessible. |
| Test Data | First Name: `Mashiat`; Last Name: `Talukder`; ZIP Code: `1212` |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the shopping cart.
4. Click **Checkout**.
5. Enter `Mashiat` in the First Name field.
6. Enter `Talukder` in the Last Name field.
7. Enter `1212` in the ZIP/Postal Code field.
8. Click **Continue**.
9. Observe the page displayed after submission.
10. Verify that the Order Overview page is displayed.

**Expected Result**

- All customer information fields accept the provided values.
- No required-field validation message is displayed.
- Clicking **Continue** proceeds to the Order Overview page.
- The selected product is displayed on the Order Overview page.
- No unexpected error message is displayed.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CHK-003: Verify Validation When All Required Fields Are Empty

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CHK-003` |
| Scenario ID | `SL-TS-CHK-003` |
| Test Case Title | Verify required-field validation when all customer information fields are empty |
| Priority | High |
| Test Type | Negative and Validation |
| Preconditions | The user is logged in, a product is in the cart, and the customer information page is displayed. |
| Test Data | First Name: empty; Last Name: empty; ZIP/Postal Code: empty |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the cart and click **Checkout**.
4. Leave the First Name field empty.
5. Leave the Last Name field empty.
6. Leave the ZIP/Postal Code field empty.
7. Click **Continue**.
8. Observe the validation message displayed.
9. Verify that the application does not proceed to the Order Overview page.

**Expected Result**

- The application prevents progression to the next checkout step.
- A validation message indicates that the First Name field is required.
- The customer information page remains displayed.
- The entered field values remain consistent with the submitted form.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CHK-004: Verify Validation When First Name Is Empty

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CHK-004` |
| Scenario ID | `SL-TS-CHK-004` |
| Test Case Title | Verify validation when the First Name field is empty |
| Priority | High |
| Test Type | Negative and Validation |
| Preconditions | The user is logged in, a product is in the cart, and the customer information page is displayed. |
| Test Data | First Name: empty; Last Name: `Talukder`; ZIP Code: `1212` |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the cart and click **Checkout**.
4. Leave the First Name field empty.
5. Enter `Talukder` in the Last Name field.
6. Enter `1212` in the ZIP/Postal Code field.
7. Click **Continue**.
8. Observe the validation message.
9. Verify that the application does not proceed to the Order Overview page.

**Expected Result**

- The application prevents progression to the next checkout step.
- A validation message indicates that the First Name field is required.
- The customer information page remains displayed.
- The valid Last Name and ZIP/Postal Code values do not bypass First Name validation.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CHK-005: Verify Validation When Last Name Is Empty

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CHK-005` |
| Scenario ID | `SL-TS-CHK-005` |
| Test Case Title | Verify validation when the Last Name field is empty |
| Priority | High |
| Test Type | Negative and Validation |
| Preconditions | The user is logged in, a product is in the cart, and the customer information page is displayed. |
| Test Data | First Name: `Mashiat`; Last Name: empty; ZIP Code: `1212` |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the cart and click **Checkout**.
4. Enter `Mashiat` in the First Name field.
5. Leave the Last Name field empty.
6. Enter `1212` in the ZIP/Postal Code field.
7. Click **Continue**.
8. Observe the validation message.
9. Verify that the application does not proceed to the Order Overview page.

**Expected Result**

- The application prevents progression to the next checkout step.
- A validation message indicates that the Last Name field is required.
- The customer information page remains displayed.
- The valid First Name and ZIP/Postal Code values do not bypass Last Name validation.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CHK-006: Verify Validation When ZIP/Postal Code Is Empty

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CHK-006` |
| Scenario ID | `SL-TS-CHK-006` |
| Test Case Title | Verify validation when the ZIP/Postal Code field is empty |
| Priority | High |
| Test Type | Negative and Validation |
| Preconditions | The user is logged in, a product is in the cart, and the customer information page is displayed. |
| Test Data | First Name: `Mashiat`; Last Name: `Talukder`; ZIP Code: empty |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the cart and click **Checkout**.
4. Enter `Mashiat` in the First Name field.
5. Enter `Talukder` in the Last Name field.
6. Leave the ZIP/Postal Code field empty.
7. Click **Continue**.
8. Observe the validation message.
9. Verify that the application does not proceed to the Order Overview page.

**Expected Result**

- The application prevents progression to the next checkout step.
- A validation message indicates that the ZIP/Postal Code field is required.
- The customer information page remains displayed.
- The valid First Name and Last Name values do not bypass ZIP/Postal Code validation.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CHK-007: Verify the Cancel Button on the Customer Information Page

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CHK-007` |
| Scenario ID | `SL-TS-CHK-007` |
| Test Case Title | Verify that Cancel returns the user to the shopping cart |
| Priority | Medium |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in, a product is in the cart, and the customer information page is displayed. |
| Test Data | Sauce Labs Backpack — $29.99 |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Open the shopping cart.
4. Click **Checkout**.
5. Verify that the customer information page is displayed.
6. Click **Cancel**.
7. Observe the page displayed after clicking Cancel.
8. Verify that the shopping cart page is displayed.
9. Verify that Sauce Labs Backpack remains in the cart.

**Expected Result**

- Clicking **Cancel** returns the user to the shopping cart page.
- The cart page is displayed successfully.
- Sauce Labs Backpack remains in the cart.
- The cart badge and cart contents remain consistent.
- The user is not advanced to the Order Overview page.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-CHK-008: Verify Checkout Behavior When the Shopping Cart Is Empty

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-CHK-008` |
| Scenario ID | `SL-TS-CHK-008` |
| Test Case Title | Verify checkout behavior with an empty shopping cart |
| Priority | Medium |
| Test Type | Functional and Negative |
| Preconditions | The user is logged in and the shopping cart contains no products. |
| Test Data | Empty cart |

**Test Steps**

1. Log in using `standard_user` and `secret_sauce`.
2. Ensure that the shopping cart contains no products.
3. Open the shopping cart page.
4. Verify that no product items are displayed.
5. Observe whether a **Checkout** button is available.
6. If the Checkout button is available, click it.
7. Observe the resulting page and any validation or error message.
8. Verify whether the application allows progression to the customer information page.
9. If the customer information page opens, observe whether the user can proceed further without adding a product.
10. Record the actual behavior at each step.

**Expected Result**

- The shopping cart displays no product items.
- The observed checkout behavior is documented accurately.
- If checkout is blocked, the application should not proceed through a purchase with no items.
- If checkout is allowed to open, record whether the application prevents progression later in the flow.
- Any unexpected behavior or error is documented for further investigation.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### Test Execution Summary — Checkout

| Metric | Count |
|---|---:|
| Total Test Cases | 8 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 8 |
| Pass Rate | Not calculated — pending execution |

###  Execution Notes

- Execute all test cases against the actual Swag Labs application.
- Record actual results only after executing the steps.
- Update each test case status based on the observed result.
- Capture screenshots for failures and unexpected behavior.
- Link reproducible defects to the corresponding test case IDs.
- For validation tests, verify the actual message text and the field identified by the application.
- For the empty-cart scenario, do not assume the checkout behavior before testing.
- Use test data only for this demo application; do not enter real personal information.

