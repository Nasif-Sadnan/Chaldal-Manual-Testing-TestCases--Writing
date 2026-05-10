# Chaldal Manual Testing Project

## Project Overview

**Chaldal** is Bangladesh's leading online grocery delivery platform, offering fast and reliable delivery of groceries, household essentials, and daily necessities directly to customers' doorsteps. This project focused on **manual testing** to verify that the platform's core features function correctly, securely, and provide a seamless user experience.

> **Tester:** MD. Nasif Sadnan Chowdhury
> **Reviewer:** Ehsanul Alam Sabbir
> **Test Period:** 29 April 2026 – 30 April 2026
> **Environment:** Production | Browser: Google Chrome

---

## Testing Scope

The manual testing process covered the following aspects of the **Chaldal Web Application**:

- **Functionality Testing:** Verification of core features including Login, Sign Up, Search, Cart, Pricing, and Delivery Address management.
- **Security Testing:** Identifying potential vulnerabilities such as exposed OTP inputs and session management issues.
- **Usability Testing:** Ensuring an intuitive, user-friendly experience across all key flows.
- **Cross-Browser Testing:** Validating compatibility across multiple browsers (Chrome, Firefox, Edge, Opera Mini, Internet Explorer).
- **Negative Testing:** Testing edge cases, invalid inputs, and boundary conditions to ensure robust validation.

---

## Testing Activities Performed

### Test Case Writing

- Created **98 detailed test cases** covering all major modules of the Chaldal application.
- Each test case includes: Test Data, Reproduction Steps, Expected Result, Actual Result, and Final Status.

### Test Plan Creation

- Developed a structured **Test Plan** outlining:
  - Testing objectives and scope
  - Test items and features covered
  - Features not included in scope
  - Test environment configuration
  - Schedule and timelines

### Mind Map

- Designed a **Mind Map** using XMind to visualize:
  - Testing strategy and approach
  - Feature coverage across all modules

### Test Scenarios

Defined **9 high-level test scenarios** to validate critical functionalities, edge cases, and boundary conditions:

| Scenario ID | Description | Priority | Test Cases |
|-------------|-------------|----------|------------|
| TS_001 | Browser compatibility across multiple browsers | P0 | 1 |
| TS_002 | Login functionality | P0 | 35 |
| TS_003 | Logout functionality | P0 | 3 |
| TS_004 | Sign Up / Registration feature | P0 | 17 |
| TS_005 | Forgot Password functionality | P0 | 12 |
| TS_006 | Search functionality | P3 | 7 |
| TS_007 | Add to Cart functionality | P0 | 11 |
| TS_008 | Pricing, Discounts & Totals | P0 | 5 |
| TS_009 | Delivery Address & Location | P0 | 7 |

### Test Metrics

Collected and analyzed **test metrics** to assess overall quality and coverage:

| # | Metric | Formula | Result |
|---|--------|---------|--------|
| 1 | Test Cases Executed | (Executed / Total) × 100 | **100%** |
| 2 | Test Cases Not Executed | (Not Executed / Total) × 100 | **0%** |
| 3 | Test Cases Passed | (Passed / Executed) × 100 | **87.76%** |
| 4 | Test Cases Failed | (Failed / Executed) × 100 | **12.24%** |
| 5 | Test Cases Blocked | (Blocked / Executed) × 100 | **0%** |

### Bug Reports

Documented **12 defects** found during testing, each with Severity, Priority, Steps to Reproduce, and Screenshot evidence:

| Bug # | Module | Issue | Priority | Severity |
|-------|--------|-------|----------|----------|
| SL-07 | Login | Mobile number field allows space characters | P3 | Minor |
| SL-30 | Login | OTP input is exposed (not masked) | P1 | **Major** |
| SL-31 | Login | OTP field not cleared after invalid OTP submission | P3 | Minor |
| SL-36 | Login | New OTP generated after resend is same as old OTP | P1 | **Critical** |
| SL-40 | Sign Up | Name field incorrectly triggers a validation error when left empty | P3 | Minor |
| SL-41 | Sign Up | Mandatory name field does not display red `*` indicator | P2 | Minor |
| SL-43 | Sign Up | Name field accepts numeric characters without error | P3 | Minor |
| SL-44 | Sign Up | Name field accepts special characters without error | P3 | Minor |
| SL-45 | Sign Up | Name field accepts numeric-special characters without error | P3 | Minor |
| SL-46 | Sign Up | No maximum character limit enforced on name field | P3 | Minor |
| SL-47 | Sign Up | No minimum character limit enforced on name field | P3 | Minor |
| SL-71 | Search | No validation error displayed when search field is submitted blank | P2 | Minor |

---

## Modules Tested

### 🔐 User Management (Login / Sign Up / Logout)
- Phone number and email-based login flows
- OTP generation, validation, expiry, resend, and masking
- Sign Up with profile details (name, email, gender)
- Input validation: empty fields, special characters, boundary values
- Logout from single and multiple devices

### 🔑 Forgot Password
- Forgot Password page accessibility and UI elements
- Registered vs. unregistered email handling
- Email delivery to inbox (not spam)
- Session termination after password update

### 🔍 Search Functionality
- Search field visibility and alignment
- Keyword search via button click and Enter key
- Paste functionality using mouse
- Pagination for multiple result pages
- Blank input validation

### 🛒 Add to Cart
- Adding single and multiple products
- Quantity increase/decrease using `+` and `–` buttons
- Auto-removal of items when quantity reaches 0
- Cart persistence across page navigation and browser refresh
- Maximum quantity enforcement
- Duplicate product handling from search and product detail page
- Cart drawer/panel interaction and empty state display

### 💰 Pricing, Discounts & Totals
- Subtotal calculation (unit price × quantity)
- Grand total calculation (subtotals + delivery charge)
- Discounted/sale price display accuracy
- Real-time cart total updates on quantity change
- Expired promotional pricing rejection at checkout

### 📍 Delivery Address & Location
- Selecting saved delivery addresses at checkout
- Adding new delivery addresses
- Handling unsupported delivery areas
- Changing delivery address during checkout
- Editing and deleting saved addresses
- Checkout prevention without address selection

---

## Testing Types Covered

| Testing Type | Description |
|---|---|
| **Functional Testing** | Verified outputs against requirements, ignoring internal implementation |
| **Integration Testing** | Validated combined functionality of integrated modules |
| **Negative Testing** | Used invalid data and incorrect inputs to break expected flows |
| **Usability Testing** | Evaluated application from a user-friendliness perspective |
| **Browser Compatibility Testing** | Ensured consistent behavior across Chrome, Firefox, Edge, Opera Mini, and IE |
| **Boundary Value Testing** | Tested lower and upper limits for input fields (e.g., name length, OTP digits) |
| **Risk-Based / Regression Testing** | Focused on high-impact, high-probability failure areas |

---

## Tools Used

| Category | Tool |
|---|---|
| Test Management | Microsoft Excel / Google Sheets |
| Mind Mapping | XMind |
| Test Environment | Google Chrome Browser (Production) |

---

## Key Outcomes

- ✅ **98 test cases executed** with **100% execution rate**
- ✅ **86 test cases passed** — achieving an **87.76% pass rate**
- 🐛 **12 defects identified and reported**, including 1 Critical and 2 Major severity bugs
- 🔒 Uncovered a **critical OTP security vulnerability** (same OTP resent on regeneration)
- 🔒 Identified **OTP masking failure** exposing sensitive input to the user
- 📋 Achieved comprehensive test coverage across **9 functional modules**
- 🌐 Validated platform compatibility across **5 major browsers**

---

## Test Execution Summary

```
┌──────────────────────────────────────────┐
│         TEST EXECUTION SUMMARY           │
├─────────────────────┬────────────────────┤
│ Total Test Cases    │         98         │
│ Passed              │    86  (87.76%)    │
│ Failed              │    12  (12.24%)    │
│ Not Executed        │     0   (0.00%)    │
│ Out of Scope        │     0   (0.00%)    │
└─────────────────────┴────────────────────┘
```
![Screenshot of Chaldal manual testing summary including test execution counts and coverage notes](https://drive.google.com/file/d/1EdkGTgH0YJyrbUrnqd0nSbZctxj2B3Pv/view?usp=sharing)

<img src="https://drive.google.com/file/d/1GRrkzVdmeckTgSEM2bQsR_AYP9wj654y/view?usp=drive_link" alt="Graph summarizing 98 test cases executed with 86 passed and 12 failed for Chaldal manual testing" width="500"/>
---

## Conclusion

This manual testing project for **Chaldal** has successfully validated the platform's core functionalities across all primary user flows — from authentication and profile management to shopping cart operations and delivery address handling. The complete documentation, including test cases, test scenarios, mind map, test metrics, and bug reports, has been prepared to support continuous quality improvement.

The two most critical findings - **OTP security exposure** and **OTP resend returning duplicate codes** - are flagged as high-priority issues requiring immediate attention to protect user account security. All other identified defects have been logged with full reproduction steps for efficient tracking and resolution.
