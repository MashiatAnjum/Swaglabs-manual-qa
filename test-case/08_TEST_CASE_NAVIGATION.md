
# Navigation Module

## Module Information

| Field | Details |
|---|---|
| Module Name | Navigation |
| Module ID | `NAV` |
| Application | Swag Labs |
| Base URL | https://www.saucedemo.com/ |
| Test Type | Functional, UI, Navigation, and Security Testing |
| Test Cases Document ID | `SL-TC-001` |
| Test Case Status | Not Run |

### Test Data

| Test Data ID | Test Data | Purpose |
|---|---|---|
| TD-NAV-001 | `standard_user` / `secret_sauce` | Access the application |
| TD-NAV-002 | Hamburger menu button; Close Menu button | Verify side navigation menu functionality |
| TD-NAV-003 | `All Items` | Verify navigation to the Inventory page |
| TD-NAV-004 | `About` | Verify navigation to the associated Sauce Labs website |
| TD-NAV-005 | `Logout` | Verify logout functionality and session termination |
| TD-NAV-006 | Sauce Labs Backpack and Sauce Labs Bike Light | Verify Reset App State functionality |
| TD-NAV-007 | Inventory, Product Details, and Cart pages | Verify browser Back and Forward navigation |

**Preconditions:** The application is accessible, and the user can log in using `standard_user` / `secret_sauce`. The user must be logged in to access the application's navigation menu and authenticated pages. Additional preconditions are specified in the individual test cases where required.

---

### TC-NAV-001: Verify Hamburger Side Navigation Menu

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-NAV-001` |
| Scenario ID | `SL-TS-NAV-001` |
| Test Case Title | Verify that the hamburger side navigation menu opens and closes correctly |
| Priority | Medium |
| Test Type | Functional and UI |
| Preconditions | The user is logged in as `standard_user` and is on the Inventory page. |
| Test Data | Hamburger menu button; Close Menu button |

**Test Steps**

1. Log in to Swag Labs using `standard_user` and `secret_sauce`.
2. Verify that the Inventory page is displayed.
3. Locate the hamburger menu icon in the upper-left corner.
4. Click the hamburger menu icon.
5. Verify that the side navigation menu opens.
6. Verify that the available menu options are displayed.
7. Locate the **Close Menu** button.
8. Click the **Close Menu** button.
9. Verify that the side navigation menu closes.

**Expected Result**

- The side navigation menu opens when the hamburger menu icon is clicked.
- All available menu options are displayed.
- The Close Menu button is visible when the menu is open.
- The side navigation menu closes when the Close Menu button is clicked.
- The Inventory page remains accessible after the menu closes.
- No unexpected UI issues occur during menu opening or closing.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-NAV-002: Verify All Items Navigation

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-NAV-002` |
| Scenario ID | `SL-TS-NAV-002` |
| Test Case Title | Verify that the All Items menu option navigates to the Inventory page |
| Priority | Medium |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in and is on another application page, such as the Cart page. |
| Test Data | Menu option: `All Items`; Expected destination: Inventory page |

**Test Steps**

1. Log in to Swag Labs using `standard_user` and `secret_sauce`.
2. Add at least one product to the cart.
3. Open the shopping cart.
4. Verify that the Cart page is displayed.
5. Open the hamburger side navigation menu.
6. Locate and click **All Items**.
7. Observe the destination page.
8. Verify that the Inventory page is displayed.
9. Verify that the Products heading and inventory product list are visible.

**Expected Result**

- Clicking **All Items** closes the side navigation menu.
- The user is redirected to the Inventory page.
- The Products heading is displayed.
- The inventory product list is displayed successfully.
- The user can interact with the available inventory controls.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-NAV-003: Verify About Menu Option

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-NAV-003` |
| Scenario ID | `SL-TS-NAV-003` |
| Test Case Title | Verify the behavior of the About menu option |
| Priority | Medium |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in and the side navigation menu is accessible. |
| Test Data | Menu option: `About`; Expected destination: Sauce Labs website |

**Test Steps**

1. Log in to Swag Labs using `standard_user` and `secret_sauce`.
2. Verify that the Inventory page is displayed.
3. Open the hamburger side navigation menu.
4. Locate the **About** menu option.
5. Click **About**.
6. Observe the destination URL.
7. Verify that the destination corresponds to the associated Sauce Labs website.
8. Verify that the destination page loads successfully.

**Expected Result**

- Clicking **About** navigates the user to the associated Sauce Labs website.
- The destination page loads successfully.
- The destination URL corresponds to the About menu option.
- No unexpected error or broken page is displayed.
- The destination URL and page behavior can be recorded during execution.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-NAV-004: Verify Logout Functionality

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-NAV-004` |
| Scenario ID | `SL-TS-NAV-004` |
| Test Case Title | Verify that clicking Logout ends the user session and redirects to the Login page |
| Priority | High |
| Test Type | Functional and Security |
| Preconditions | The user is logged in as `standard_user` and is on an authenticated application page. |
| Test Data | Menu option: `Logout`; Expected destination: Login page |

**Test Steps**

1. Log in to Swag Labs using `standard_user` and `secret_sauce`.
2. Verify that the Inventory page is displayed.
3. Open the hamburger side navigation menu.
4. Locate the **Logout** option.
5. Click **Logout**.
6. Verify that the Login page is displayed.
7. Observe the current application URL.
8. Attempt to access the Inventory page directly using the browser's address bar without logging in.
9. Observe the application's response.
10. Verify whether access to the protected application content is restricted.

**Expected Result**

- Clicking **Logout** redirects the user to the Login page.
- The authenticated user session is terminated.
- The user cannot access protected application content without logging in again.
- Direct access to the Inventory page without authentication is restricted.
- No authenticated application content is accessible after logout.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-NAV-005: Verify Reset App State Functionality

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-NAV-005` |
| Scenario ID | `SL-TS-NAV-005` |
| Test Case Title | Verify that Reset App State resets the cart and product-selection state |
| Priority | Medium |
| Test Type | Functional |
| Preconditions | The user is logged in and at least one product has been added to the cart. |
| Test Data | Sauce Labs Backpack and Sauce Labs Bike Light; Menu option: `Reset App State` |

**Test Steps**

1. Log in to Swag Labs using `standard_user` and `secret_sauce`.
2. Add Sauce Labs Backpack to the cart.
3. Add Sauce Labs Bike Light to the cart.
4. Verify that the cart badge reflects the selected products.
5. Open the hamburger side navigation menu.
6. Locate the **Reset App State** option.
7. Click **Reset App State**.
8. Close the side navigation menu if it remains open.
9. Inspect the cart badge.
10. Verify whether the cart badge is cleared or no longer displayed.
11. Open the shopping cart.
12. Verify that the previously selected products are no longer present.
13. Return to the Inventory page if necessary.
14. Verify the product-selection buttons for the previously selected products.

**Expected Result**

- The cart badge is cleared or no longer displayed when the cart is empty.
- The previously selected products are removed from the active cart.
- The product-selection state is reset according to the application's behavior.
- The previously selected products display their initial selection state.
- The user remains logged in after resetting the application state.
- No unexpected error occurs during the reset operation.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### TC-NAV-006: Verify Browser Back and Forward Navigation

| Field | Details |
|---|---|
| Test Case ID | `SL-TC-NAV-006` |
| Scenario ID | `SL-TS-NAV-006` |
| Test Case Title | Verify browser back and forward navigation behavior across relevant application pages |
| Priority | Medium |
| Test Type | Functional and Navigation |
| Preconditions | The user is logged in as `standard_user` and can access the Inventory, Product Details, and Cart pages. |
| Test Data | Pages: Inventory, Product Details, and Cart; Browser controls: Back and Forward |

**Test Steps**

1. Log in to Swag Labs using `standard_user` and `secret_sauce`.
2. Verify that the Inventory page is displayed.
3. Click a product name or image to open its Product Details page.
4. Verify that the Product Details page is displayed.
5. Navigate to the Cart page.
6. Verify that the Cart page is displayed.
7. Click the browser's **Back** button.
8. Verify that the previously visited Product Details page is displayed.
9. Click the browser's **Back** button again.
10. Verify that the Inventory page is displayed.
11. Click the browser's **Forward** button.
12. Verify that the Product Details page is displayed.
13. Click the browser's **Forward** button again.
14. Verify that the Cart page is displayed.

**Expected Result**

- Browser Back and Forward navigation follow the application's page history.
- Clicking Back from the Cart page returns the user to the Product Details page.
- Clicking Back again returns the user to the Inventory page.
- Clicking Forward restores the Product Details page.
- Clicking Forward again restores the Cart page.
- The displayed page corresponds to the relevant browser navigation-history entry.
- No unexpected error page or broken application state is displayed.
- Any behavior involving authentication or cart state is recorded during execution.

**Actual Result:** Not recorded — pending execution.

**Status:** Not Run.

**Evidence:** Pending.

---

### Test Execution Summary — Navigation

| Metric | Count |
|---|---:|
| Total Test Cases | 6 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 6 |
| Pass Rate | Not calculated — pending execution |

### Execution Notes

- Execute all test cases against the actual Swag Labs application.
- Record actual results only after performing the test steps.
- Update each test case status based on the observed result.
- Capture screenshots of the navigation menu and relevant destination pages.
- Verify the opening and closing behavior of the hamburger side navigation menu.
- Verify that each navigation option redirects to its expected destination.
- Confirm that Logout terminates the authenticated session.
- Verify that Reset App State clears the cart and resets product-selection states.
- Test browser Back and Forward navigation across the relevant application pages.
- Record any unexpected navigation behavior or application state changes.
- Report reproducible defects and link them to the corresponding test case ID.
- Do not change the expected result merely to match an unexpected application result.
