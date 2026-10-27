
## 1. Document Information

| Field | Details |
|---|---|
| Project Name | Swag Labs Manual QA Case Study |
| Document ID | SL-TC-001 |
| Version | 1.0 |
| Status | Draft — Pending Test Execution |
| Prepared By | Mashiat Anjum Talukder |
| Application URL | https://www.saucedemo.com/ |
| Created Date | 27 October 2026 |
| Test Type | Manual Functional Testing |
| Module | Login / Authentication |

## 2. Introduction

This document contains detailed manual test cases for the Login module of the Swag Labs e-commerce web application.

The test cases are derived from the Login scenarios documented in `SL-TS-001.md`. They cover successful authentication, invalid credentials, empty-field validation, locked-out accounts, and special demo-user behavior.

Each test case includes its preconditions, test data, execution steps, expected result, actual result, status, and evidence reference.

## 3. Test Environment

| Item | Configuration |
|---|---|
| Application | Swag Labs |
| URL | https://www.saucedemo.com/ |
| Operating System | Windows — 11 |
| Browser | Google Chrome — 155 |
| Testing Method | Manual Testing |
| Test Environment | Public Demo Application |

## 4. Test Data

| Data ID | Username | Password | Purpose |
|---|---|---|---|
| TD-LOG-001 | `standard_user` | `secret_sauce` | Valid standard-user credentials |
| TD-LOG-002 | `invalid_user` | `invalid_password` | Invalid credentials |
| TD-LOG-003 | Empty | Empty | Both fields empty |
| TD-LOG-004 | Empty | `secret_sauce` | Username empty |
| TD-LOG-005 | `standard_user` | Empty | Password empty |
| TD-LOG-006 | `locked_out_user` | `secret_sauce` | Locked-out user |
| TD-LOG-007 | `problem_user` | `secret_sauce` | Problem user behavior |
| TD-LOG-008 | `performance_glitch_user` | `secret_sauce` | Performance glitch user behavior |

**Note:** These are commonly documented public demo credentials and test inputs. Verify account availability and behavior during execution. The invalid username and password are intentionally fabricated test data.

## 5. Detailed Test Cases

### TC-LOG-001: Successful Login with Valid Credentials

| Field | Details |
|---|---|
| Test Case ID | SL-TC-LOG-001 |
| Scenario ID | SL-TS-LOG-001 |
| Test Case Title | Verify successful login with valid standard-user credentials |
| Priority | High |
| Test Type | Positive Testing |
| Preconditions | The login page is accessible, and the standard demo account is available. |
| Test Data | TD-LOG-001 |

**Test Steps**

1. Open https://www.saucedemo.com/.
2. Enter `standard_user` in the Username field.
3. Enter `secret_sauce` in the Password field.
4. Click the Login button.

**Expected Result**

- The user is successfully authenticated.
- The application redirects to the inventory page.
- The inventory page displays the available products.
- No login error message is displayed.

| Field | Result |
|---|---|
| Actual Result | Not recorded — pending execution |
| Status | Not Run |
| Evidence | Pending — add screenshot reference after execution |

---

### TC-LOG-002: Login with Invalid Credentials

| Field | Details |
|---|---|
| Test Case ID | SL-TC-LOG-002 |
| Scenario ID | SL-TS-LOG-002 |
| Test Case Title | Verify login behavior with invalid credentials |
| Priority | High |
| Test Type | Negative Testing |
| Preconditions | The login page is accessible. |
| Test Data | TD-LOG-002 |

**Test Steps**

1. Open https://www.saucedemo.com/.
2. Enter `invalid_user` in the Username field.
3. Enter `invalid_password` in the Password field.
4. Click the Login button.

**Expected Result**

- The application rejects the invalid credentials.
- The user remains on the login page.
- An appropriate login error message is displayed.
- The inventory page is not accessible through this failed login attempt.

| Field | Result |
|---|---|
| Actual Result | Not recorded — pending execution |
| Status | Not Run |
| Evidence | Pending — add screenshot reference after execution |

---

### TC-LOG-003: Login with Both Fields Empty

| Field | Details |
|---|---|
| Test Case ID | SL-TC-LOG-003 |
| Scenario ID | SL-TS-LOG-003 |
| Test Case Title | Verify validation when both username and password fields are empty |
| Priority | High |
| Test Type | Negative Testing |
| Preconditions | The login page is accessible. |
| Test Data | TD-LOG-003 |

**Test Steps**

1. Open https://www.saucedemo.com/.
2. Leave the Username field empty.
3. Leave the Password field empty.
4. Click the Login button.

**Expected Result**

- The application does not authenticate the user.
- The user remains on the login page.
- A validation error message indicates that the username is required.

| Field | Result |
|---|---|
| Actual Result | Not recorded — pending execution |
| Status | Not Run |
| Evidence | Pending — add screenshot reference after execution |

---

### TC-LOG-004: Login with Empty Username

| Field | Details |
|---|---|
| Test Case ID | SL-TC-LOG-004 |
| Scenario ID | SL-TS-LOG-004 |
| Test Case Title | Verify validation when the username field is empty |
| Priority | High |
| Test Type | Negative Testing |
| Preconditions | The login page is accessible. |
| Test Data | TD-LOG-004 |

**Test Steps**

1. Open https://www.saucedemo.com/.
2. Leave the Username field empty.
3. Enter `secret_sauce` in the Password field.
4. Click the Login button.

**Expected Result**

- The application does not authenticate the user.
- The user remains on the login page.
- A validation error message indicates that the username is required.

| Field | Result |
|---|---|
| Actual Result | Not recorded — pending execution |
| Status | Not Run |
| Evidence | Pending — add screenshot reference after execution |

---

### TC-LOG-005: Login with Empty Password

| Field | Details |
|---|---|
| Test Case ID | SL-TC-LOG-005 |
| Scenario ID | SL-TS-LOG-005 |
| Test Case Title | Verify validation when the password field is empty |
| Priority | High |
| Test Type | Negative Testing |
| Preconditions | The login page is accessible. |
| Test Data | TD-LOG-005 |

**Test Steps**

1. Open https://www.saucedemo.com/.
2. Enter `standard_user` in the Username field.
3. Leave the Password field empty.
4. Click the Login button.

**Expected Result**

- The application does not authenticate the user.
- The user remains on the login page.
- A validation error message indicates that the password is required.

| Field | Result |
|---|---|
| Actual Result | Not recorded — pending execution |
| Status | Not Run |
| Evidence | Pending — add screenshot reference after execution |

---

### TC-LOG-006: Login with a Locked-Out User Account

| Field | Details |
|---|---|
| Test Case ID | SL-TC-LOG-006 |
| Scenario ID | SL-TS-LOG-006 |
| Test Case Title | Verify login behavior for a locked-out user |
| Priority | Medium |
| Test Type | Negative Testing |
| Preconditions | The login page is accessible, and the locked-out demo account is available. |
| Test Data | TD-LOG-006 |

**Test Steps**

1. Open https://www.saucedemo.com/.
2. Enter `locked_out_user` in the Username field.
3. Enter `secret_sauce` in the Password field.
4. Click the Login button.

**Expected Result**

- The application rejects the login attempt for the locked-out account.
- The user remains on the login page.
- An appropriate error message explains that the account is locked out.

| Field | Result |
|---|---|
| Actual Result | Not recorded — pending execution |
| Status | Not Run |
| Evidence | Pending — add screenshot reference after execution |

---

### TC-LOG-007: Login with the Problem User Account

| Field | Details |
|---|---|
| Test Case ID | SL-TC-LOG-007 |
| Scenario ID | SL-TS-LOG-007 |
| Test Case Title | Verify login and subsequent application behavior for the problem user |
| Priority | Medium |
| Test Type | Special Test-User Behavior |
| Preconditions | The login page is accessible, and the problem-user demo account is available. |
| Test Data | TD-LOG-007 |

**Test Steps**

1. Open https://www.saucedemo.com/.
2. Enter `problem_user` in the Username field.
3. Enter `secret_sauce` in the Password field.
4. Click the Login button.
5. Observe whether login succeeds.
6. If login succeeds, inspect the inventory page for product images, names, descriptions, prices, and other visible inconsistencies.
7. Record any unexpected behavior with reproducible steps and supporting evidence.

**Expected Result**

- The application responds consistently with the behavior observed for the problem-user account.
- Any differences in product display or functionality are recorded accurately.
- Any suspected defect is documented only after it has been observed and reproduced.

| Field | Result |
|---|---|
| Actual Result | Not recorded — pending execution |
| Status | Not Run |
| Evidence | Pending — add screenshots of observed behavior |

---

### TC-LOG-008: Login with the Performance Glitch User Account

| Field | Details |
|---|---|
| Test Case ID | SL-TC-LOG-008 |
| Scenario ID | SL-TS-LOG-008 |
| Test Case Title | Verify login behavior for the performance glitch user |
| Priority | Medium |
| Test Type | Special Test-User Behavior |
| Preconditions | The login page is accessible, and the performance-glitch demo account is available. |
| Test Data | TD-LOG-008 |

**Test Steps**

1. Open https://www.saucedemo.com/.
2. Enter `performance_glitch_user` in the Username field.
3. Enter `secret_sauce` in the Password field.
4. Click the Login button.
5. Observe the time taken for the login operation to complete.
6. Verify whether the inventory page eventually loads.
7. Record any unexpected delays, loading issues, or functional problems.

**Expected Result**

- The login operation completes or fails in an observable and reproducible manner.
- If login succeeds, the inventory page is displayed.
- Any unusual delay or functional issue is documented with the observed behavior and available evidence.
- No arbitrary performance threshold is assumed unless a measurable acceptance criterion has been defined.

| Field | Result |
|---|---|
| Actual Result | Not recorded — pending execution |
| Status | Not Run |
| Evidence | Pending — add screenshot or timing record after execution |

## 6. Test Execution Summary

Complete this section after executing the test cases.

| Metric | Count |
|---|---:|
| Total Test Cases | 8 |
| Passed | 0 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 8 |
| Pass Rate | Not calculated — no tests executed |

**Pass Rate Formula**

Pass Rate = (Passed Test Cases / Executed Test Cases) × 100

Blocked and Not Run test cases should not be counted as executed tests. Report the denominator used when presenting execution metrics.

## 7. Defect Reporting Guidelines

If a test case fails:

- Reproduce the unexpected behavior.
- Record the actual result and compare it with the expected result.
- Capture supporting evidence where practical.
- Create a separate defect report using the project convention `SL-BR-001`, `SL-BR-002`, and so on.
- Include the related test case ID in the defect report.
- Assign severity and priority based on impact and urgency.

A difference from the expected result is not automatically a confirmed application defect. Investigate and document the observed behavior first, especially for intentionally unusual demo accounts.

## 8. Document Status

**Prepared By:** Mashiat Anjum Talukder

**Review Status:** Pending Self-Review

**Approval Status:** Not Applicable — Independent Portfolio Project

**Execution Status:** Not Started

