
## Order Completion Module

### TC-OCM-001: Complete Order Successfully

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-OCM-001 |
| **Scenario ID** | SL-TS-OCM-001 |
| **Test Case Title** | Verify that clicking the Finish button completes the order successfully |
| **Priority** | High |
| **Test Type** | Functional |
| **Preconditions** | User is logged in as `standard_user`, has added at least one product to the cart, and has proceeded through checkout to the Order Overview page with valid customer information. |
| **Test Data** | Product: Sauce Labs Backpack; First Name: Mashiat; Last Name: Talukder; ZIP Code: 1212 |

**Test Steps:**
1. Log in to the application using valid credentials.
2. Add the Sauce Labs Backpack to the cart.
3. Open the cart and click **Checkout**.
4. Enter valid customer information and click **Continue**.
5. Verify that the Order Overview page is displayed.
6. Click the **Finish** button.

**Expected Result:**
- The order is completed successfully.
- The user is redirected to the Order Completion page.
- The page displays the order confirmation content.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### TC-OCM-002: Verify Order Confirmation Header

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-OCM-002 |
| **Scenario ID** | SL-TS-OCM-002 |
| **Test Case Title** | Verify the order confirmation header |
| **Priority** | High |
| **Test Type** | UI / Functional |
| **Preconditions** | User has successfully completed checkout and reached the Order Completion page. |
| **Test Data** | Expected header: `Thank you for your order!` |

**Test Steps:**
1. Complete the checkout process with valid information.
2. Click **Finish** on the Order Overview page.
3. Locate the order confirmation header.
4. Verify the displayed text against the expected header.

**Expected Result:**
- The Order Completion page is displayed.
- The confirmation header reads exactly **"Thank you for your order!"**.
- The header is clearly visible to the user.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### TC-OCM-003: Verify Order Confirmation Message

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-OCM-003 |
| **Scenario ID** | SL-TS-OCM-003 |
| **Test Case Title** | Verify the order confirmation message |
| **Priority** | Medium |
| **Test Type** | Functional / UI |
| **Preconditions** | User has successfully completed checkout and reached the Order Completion page. |
| **Test Data** | Expected message: `Your order has been dispatched, and will arrive just as fast as the pony can get there!` |

**Test Steps:**
1. Complete the checkout process with valid information.
2. Click **Finish** on the Order Overview page.
3. Locate the order confirmation message beneath the confirmation header.
4. Verify the displayed message against the expected text.

**Expected Result:**
- The order confirmation message is displayed.
- The message matches the expected text.
- The message is readable and visible on the page.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### TC-OCM-004: Verify Back Home Navigation

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-OCM-004 |
| **Scenario ID** | SL-TS-OCM-004 |
| **Test Case Title** | Verify that the Back Home button redirects to the Inventory page |
| **Priority** | High |
| **Test Type** | Functional / Navigation |
| **Preconditions** | User has successfully completed checkout and is on the Order Completion page. |
| **Test Data** | Button: `Back Home`; Expected destination: Inventory page |

**Test Steps:**
1. Complete the checkout process with valid information.
2. Click **Finish** on the Order Overview page.
3. Verify that the Order Completion page is displayed.
4. Click the **Back Home** button.
5. Verify the destination page and its displayed products.

**Expected Result:**
- The user is redirected to the Inventory page.
- The product listing is displayed.
- The user can interact with the available inventory controls.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### TC-OCM-005: Verify Cart State After Order Completion

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-OCM-005 |
| **Scenario ID** | SL-TS-OCM-005 |
| **Test Case Title** | Verify that the cart badge and active cart state are cleared after successful order completion |
| **Priority** | High |
| **Test Type** | Functional |
| **Preconditions** | User has added one or more products to the cart and is on the Order Overview page before completing checkout. |
| **Test Data** | Products: Sauce Labs Backpack and Sauce Labs Bike Light |

**Test Steps:**
1. Log in using valid credentials.
2. Add the Sauce Labs Backpack and Sauce Labs Bike Light to the cart.
3. Open the cart and verify that both products are present.
4. Proceed through checkout using valid customer information.
5. Click **Finish** on the Order Overview page.
6. Verify that the Order Completion page is displayed.
7. Click **Back Home** to return to the Inventory page.
8. Inspect the cart badge and open the cart.

**Expected Result:**
- The cart badge is no longer displayed when the cart is empty.
- The previously purchased products are no longer present in the active cart.
- The cart contents reflect the cleared state after successful order completion.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

