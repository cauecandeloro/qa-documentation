
# Test Cases — Restful Booker

## Auth

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-001 | Generate authentication token | API is accessible | 1. Send POST to /auth with valid credentials | Response contains a token string | ✅ Pass |

---

## Bookings

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-002 | Get all bookings | API is accessible | 1. Send GET to /booking | Response is a non-empty array of booking IDs | ✅ Pass |
| TC-003 | Get booking by ID | API is accessible | 1. Send GET to /booking/{{booking_id}} | Response contains firstname, lastname, totalprice and booking dates | ✅ Pass |

---

## Create Booking

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-004 | Create booking with valid data | API is accessible | 1. Send POST to /booking with valid body 2. Include firstname, lastname, totalprice, depositpaid, bookingdates and additionalneeds | Response contains bookingid and booking data matching the request | ✅ Pass |

---

## Update Booking

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-005 | Update existing booking | Valid token and booking ID available | 1. Send PUT to /booking/{{new_booking_id}} 2. Include updated firstname, totalprice and checkout date 3. Include Cookie header with token | Response contains updated booking data | ✅ Pass |

---

## Delete Booking

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-006 | Delete existing booking | Valid token and booking ID available | 1. Send DELETE to /booking/{{new_booking_id}} 2. Include Cookie header with token | Response status is 201 | ✅ Pass |
