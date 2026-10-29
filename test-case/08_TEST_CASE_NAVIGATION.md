
##  Navigation Module

### SL-TC-NAV-001: Verify Hamburger Side Navigation Menu

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-NAV-001 |
| **Scenario ID** | SL-TS-NAV-001 |
| **Test Case Title** | Verify that the hamburger side navigation menu opens and closes correctly |
| **Priority** | Medium |
| **Test Type** | Functional / UI |
| **Preconditions** | User is logged in as `standard_user` and is on the Inventory page. |
| **Test Data** | Hamburger menu button; Close Menu button |

**Test Steps:**
1. Log in to Swag Labs using valid credentials.
2. Click the hamburger menu icon in the upper-left corner.
3. Verify that the side navigation menu opens.
4. Verify that the menu options are visible.
5. Click the **Close Menu** button.
6. Verify that the side navigation menu closes.

**Expected Result:**
- The side navigation menu opens when the hamburger menu icon is clicked.
- The available menu options are displayed.
- The menu closes when the Close Menu button is clicked.
- The Inventory page remains accessible after the menu closes.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### SL-TC-NAV-002: Verify All Items Navigation

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-NAV-002 |
| **Scenario ID** | SL-TS-NAV-002 |
| **Test Case Title** | Verify that the All Items menu option navigates to the Inventory page |
| **Priority** | Medium |
| **Test Type** | Functional / Navigation |
| **Preconditions** | User is logged in and is on another application page, such as the Cart page. |
| **Test Data** | Menu option: `All Items`; Expected destination: Inventory page |

**Test Steps:**
1. Log in to Swag Labs using valid credentials.
2. Navigate to the Cart page.
3. Open the hamburger side navigation menu.
4. Click **All Items**.
5. Verify the destination page.

**Expected Result:**
- The side navigation menu closes.
- The user is redirected to the Inventory page.
- The inventory product list is displayed.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### SL-TC-NAV-003: Verify About Menu Option

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-NAV-003 |
| **Scenario ID** | SL-TS-NAV-003 |
| **Test Case Title** | Verify the behavior of the About menu option |
| **Priority** | Medium |
| **Test Type** | Functional / Navigation |
| **Preconditions** | User is logged in and the side navigation menu is accessible. |
| **Test Data** | Menu option: `About`; Expected destination: Sauce Labs website |

**Test Steps:**
1. Log in to Swag Labs using valid credentials.
2. Open the hamburger side navigation menu.
3. Click **About**.
4. Observe the destination URL and the page that loads.
5. Verify that the destination corresponds to the About option.

**Expected Result:**
- Clicking About navigates the user to the associated Sauce Labs website.
- The destination page loads successfully.
- The destination URL and page behavior are recorded during execution.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### SL-TC-NAV-004: Verify Logout Functionality

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-NAV-004 |
| **Scenario ID** | SL-TS-NAV-004 |
| **Test Case Title** | Verify that clicking Logout ends the user session and redirects to the Login page |
| **Priority** | High |
| **Test Type** | Functional / Security |
| **Preconditions** | User is logged in as `standard_user` and is on an authenticated application page. |
| **Test Data** | Menu option: `Logout`; Expected destination: Login page |

**Test Steps:**
1. Log in to Swag Labs using valid credentials.
2. Open the hamburger side navigation menu.
3. Click **Logout**.
4. Verify that the Login page is displayed.
5. Attempt to access the Inventory page using the browser's address bar without logging in.
6. Verify the application's response.

**Expected Result:**
- The user is redirected to the Login page after logout.
- The authenticated session is ended.
- The user cannot access protected application content without logging in again.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### SL-TC-NAV-005: Verify Reset App State Functionality

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-NAV-005 |
| **Scenario ID** | SL-TS-NAV-005 |
| **Test Case Title** | Verify that Reset App State resets the cart and product-selection state |
| **Priority** | Medium |
| **Test Type** | Functional |
| **Preconditions** | User is logged in and at least one product has been added to the cart. |
| **Test Data** | Products: Sauce Labs Backpack and Sauce Labs Bike Light; Menu option: `Reset App State` |

**Test Steps:**
1. Log in to Swag Labs using valid credentials.
2. Add the Sauce Labs Backpack and Sauce Labs Bike Light to the cart.
3. Verify that the cart badge reflects the selected products.
4. Open the hamburger side navigation menu.
5. Click **Reset App State**.
6. Close the side navigation menu if it remains open.
7. Check the cart badge.
8. Open the Cart page and verify the cart contents.
9. Verify the product-selection buttons on the Inventory page.

**Expected Result:**
- The cart badge is cleared or no longer displayed when the cart is empty.
- The previously selected products are removed from the active cart.
- The product-selection state is reset according to the application's behavior.
- The user remains logged in unless the application behaves otherwise.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

---

### SL-TC-NAV-006: Verify Browser Back and Forward Navigation

| Field | Details |
|---|---|
| **Test Case ID** | SL-TC-NAV-006 |
| **Scenario ID** | SL-TS-NAV-006 |
| **Test Case Title** | Verify browser back and forward navigation behavior across relevant application pages |
| **Priority** | Medium |
| **Test Type** | Functional / Navigation |
| **Preconditions** | User is logged in as `standard_user` and can access the Inventory, Product Details, and Cart pages. |
| **Test Data** | Pages: Inventory, Product Details, Cart; Browser controls: Back and Forward |

**Test Steps:**
1. Log in to Swag Labs and verify that the Inventory page is displayed.
2. Click a product name or image to open its Product Details page.
3. Navigate to the Cart page.
4. Click the browser's **Back** button.
5. Verify the page displayed.
6. Click the browser's **Back** button again.
7. Verify the page displayed.
8. Click the browser's **Forward** button.
9. Verify the page displayed.
10. Click the browser's **Forward** button again.
11. Verify the page displayed.

**Expected Result:**
- Browser Back and Forward navigation follow the application's page history.
- The displayed page corresponds to the relevant navigation-history entry.
- No unexpected error page or broken application state is displayed.
- Any behavior involving authentication or cart state is recorded during execution.

| Actual Result | Status | Evidence |
|---|---|---|
| Not recorded — pending execution | Not Run | Pending |

