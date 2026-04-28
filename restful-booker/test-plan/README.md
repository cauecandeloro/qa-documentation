
# Test Plan — Restful Booker

## 1. Overview

This test plan describes the testing strategy for the Restful Booker API,
a public REST API available at https://restful-booker.herokuapp.com, built
for testing purposes and used as a reference for API testing practice and
portfolio demonstration.

---

## 2. Objectives

- Validate the main CRUD operations of the API
- Ensure authentication works correctly
- Verify response bodies, status codes and data integrity
- Demonstrate API testing skills using Postman

---

## 3. Scope

### In Scope
- Authentication — token generation
- Booking retrieval — get all bookings and get by ID
- Booking creation — create new bookings
- Booking update — full update of existing bookings
- Booking deletion — delete existing bookings

### Out of Scope
- Performance testing
- Security testing
- UI testing

---

## 4. Test Approach

| Type | Description |
|---|---|
| Functional Testing | Validate API endpoints against expected behavior |
| Integration Testing | Validate data flow between requests using dynamic variables |
| Regression Testing | Ensure existing endpoints work after changes |

---

## 5. Test Environment

| Item | Details |
|---|---|
| API Base URL | https://restful-booker.herokuapp.com |
| Tool | Postman |
| Test Scripts | JavaScript |
| CI/CD | Collection Runner |

---

## 6. Test Credentials

| Field | Value |
|---|---|
| Username | admin |
| Password | password123 |

---

## 7. Entry and Exit Criteria

### Entry Criteria
- API is accessible and responding
- Postman collection and environment are configured
- Authentication token can be generated successfully

### Exit Criteria
- All planned test cases have been executed
- All critical and high severity bugs have been resolved
- Collection Runner report has been generated

---

## 8. Deliverables

- Test Plan (this document)
- Test Cases
- Bug Reports
- Automated API test collection — [postman-restfulbooker](https://github.com/cauecandeloro/postman-restfulbooker)

---

## 9. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| API public instability | High | Regenerate token and recreate booking before each test run |
| Booking expiration | Medium | Always run Create Booking before Update and Delete |
| Shared environment with other users | Low | Use dynamic variables to avoid ID conflicts |
