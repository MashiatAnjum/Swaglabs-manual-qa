Test Plan — Swag Labs E-commerce Application

## 1. Document Information

| Field | Details |
|---|---|
| Project Name | Swag Labs Manual QA Case Study |
| Document ID | SL-TP-001 |
| Version | 1.0 |
| Status | Draft — pending test execution |
| Prepared By | Mashiat Anjum Talukder |
| Application URL | [https://www.saucedemo.com/](https://www.saucedemo.com/) |
| Created Date | 25 October 2026 |
| Test Type | Manual Functional Testing |

## 2. Introduction

This document defines the scope, objectives, approach, test environment, and completion criteria for manual testing of the Swag Labs e-commerce web application.

The project simulates a basic online shopping experience, allowing a tester to practise validating authentication, product browsing, shopping cart functionality, and checkout workflows.

## 3. Objectives

Validate core shopping workflows from login through cart management.

Verify expected behaviour for positive and negative inputs.

Identify, document, and report reproducible defects.

Practise professional test planning, test design, execution, and reporting.

Establish a manual test baseline that can later be automated using Python.

## 4. Application Under Test

Application: Sauce Demo / Swag Labs
URL: https://www.saucedemo.com/

The application is a public testing storefront. Before execution, confirm that the login page and the intended features are available in the current version.

## 5. Scope of Testing

# In scope

Authentication

Login page loads correctly.

Login with valid and invalid credentials.

Empty username and password validation.

Appropriate error messages for rejected login attempts.

Product Listing

Product inventory page loads after successful login.

Product names, descriptions, images, and prices are displayed.

Product detail pages open correctly.

Product sorting works, if available.

Shopping Cart

Add a product to the cart.

Verify the cart badge/count, if displayed.

Open the cart and verify selected products.

Remove a product from the cart.

Verify cart state after adding or removing items.

Checkout — initial coverage

Checkout page opens from the cart.

Required customer information is validated.

Valid test information allows progression to the next step.

Order summary and completion behaviour are checked if time permits.

Basic usability

Important controls and validation messages are visible.

Core actions can be completed using a desktop browser.

Basic keyboard operation is checked where practical.

# Out of scope

Production e-commerce systems or real purchases.

Payment gateway or financial transaction testing.

Security penetration testing.

Load, stress, and performance testing.

API testing and automated testing during the initial manual phase.

Exhaustive cross-browser and accessibility certification.

## 6. Test Approach

The following techniques will be used:

Positive testing

Negative testing

Equivalence partitioning

Boundary-value analysis where applicable

Exploratory testing

Functional testing

Basic usability checks

Retesting and regression checks when a defect or change is identified

Testing will begin with the login workflow, followed by product browsing and cart operations. Checkout will be included after the earlier workflows are understood.
