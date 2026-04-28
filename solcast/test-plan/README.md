
# Test Plan — Solcast Website

## 1. Overview

This test plan describes the testing strategy for the Solcast institutional
website, available at https://solcast.com.br. Solcast is a Brazilian technology
company specializing in BIaaS (Business Intelligence as a Service).

---

## 2. Objectives

- Validate the main navigation flows of the website
- Ensure key content elements are correctly displayed
- Validate contact form field behavior without submitting
- Verify responsive behavior across desktop and mobile viewports
- Identify and document defects found during testing

---

## 3. Scope

### In Scope
- Navigation — menu links and page routing
- Homepage — key content elements visibility
- Contact form — field validation without form submission
- Responsive layout — desktop and mobile viewports

### Out of Scope
- Form submission and backend processing
- Performance testing
- Security testing
- Content accuracy review

---

## 4. Test Approach

| Type | Description |
|---|---|
| Functional Testing | Validate navigation and content against expected behavior |
| UI Testing | Verify visibility of key interface elements |
| Responsive Testing | Validate layout on desktop and mobile viewports |
| Cross-browser Testing | Execute tests on Chromium, Firefox and WebKit |
| Automated Testing | E2E tests using Playwright and TypeScript |

---

## 5. Test Environment

| Item | Details |
|---|---|
| Application URL | https://solcast.com.br |
| Browsers | Chromium, Firefox, WebKit |
| Automation Framework | Playwright |
| Language | TypeScript |
| CI/CD | GitHub Actions |
| Viewports | Desktop: 1280x800 / Mobile: 375x812 |

---

## 6. Entry and Exit Criteria

### Entry Criteria
- Website is accessible and stable
- Test environment is configured
- Test cases are reviewed and approved

### Exit Criteria
- All planned test cases have been executed
- All critical and high severity bugs have been resolved
- Test summary report has been generated

---

## 7. Deliverables

- Test Plan (this document)
- Test Cases
- Bug Reports
- Automated test suite — [playwright-solcast](https://github.com/cauecandeloro/playwright-solcast)

---

## 8. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Website content changes | Medium | Review selectors after any website update |
| Browser compatibility issues | Medium | Run tests across all three supported browsers |
| Cookie consent banner interference | Low | Handle banner dismissal in test setup if needed |
