# Test Plan — Sauce Demo

## 1. Overview

This test plan describes the testing strategy for the Sauce Demo web application,
an e-commerce platform available at https://www.saucedemo.com, used as a reference
application for QA practice and portfolio demonstration.

---

## 2. Objectives

- Validate the main user flows of the application
- Ensure the application behaves correctly across different browsers
- Identify and document defects found during testing
- Demonstrate test coverage across functional and non-functional requirements

---

## 3. Scope

### In Scope
- Login and authentication
- Product inventory and sorting
- Shopping cart management
- Checkout flow
- Logout

### Out of Scope
- Performance testing
- Security testing
- Backend/API testing

---

## 4. Test Approach

| Type | Description |
|---|---|
| Functional Testing | Validate features against requirements |
| Regression Testing | Ensure new changes do not break existing functionality |
| Cross-browser Testing | Execute tests on Chromium, Firefox and WebKit |
| Automated Testing | E2E tests using Playwright and TypeScript |

---

## 5. Test Environment

| Item | Details |
|---|---|
| Application URL | https://www.saucedemo.com |
| Browsers | Chromium, Firefox, WebKit |
| Automation Framework | Playwright |
| Language | TypeScript |
| CI/CD | GitHub Actions |

---

## 6. Test Credentials

| User | Password | Description |
|---|---|---|
| standard_user | secret_sauce | Standard user with full access |
| locked_out_user | secret_sauce | User blocked from logging in |
| problem_user | secret_sauce | User with UI display issues |

---

## 7. Entry and Exit Criteria

### Entry Criteria
- Application is accessible and stable
- Test environment is configured
- Test cases are reviewed and approved

### Exit Criteria
- All planned test cases have been executed
- All critical and high severity bugs have been resolved
- Test summary report has been generated

---

## 8. Deliverables

- Test Plan (this document)
- Test Cases
- Bug Reports
- Automated test suite (playwright-saucedemo repository)

---

## 9. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Application instability | High | Monitor availability before test execution |
| Browser compatibility issues | Medium | Run tests across all three supported browsers |
| Test data dependency | Low | Use predefined credentials provided by the application |
