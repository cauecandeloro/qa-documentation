
# Bug Reports — Restful Booker

## BUG-001 — Delete endpoint returns 201 instead of 200

| Field | Details |
|---|---|
| **ID** | BUG-001 |
| **Title** | Delete endpoint returns 201 Created instead of 200 OK |
| **Module** | Delete Booking |
| **Severity** | Low |
| **Priority** | Low |
| **Status** | Open |
| **Environment** | Postman |

### Steps to Reproduce
1. Generate a valid authentication token via POST /auth
2. Create a new booking via POST /booking
3. Send DELETE to /booking/{{bookingid}} with Cookie header containing the token

### Expected Result
Response status code is 200 OK confirming the booking was successfully deleted.

### Actual Result
Response status code is 201 Created, which semantically refers to resource creation, not deletion.

### Notes
While the deletion is performed correctly, the use of HTTP 201 for a DELETE operation is inconsistent with REST API standards. According to REST conventions, a successful deletion should return 200 OK or 204 No Content.

---

## BUG-002 — Token expires quickly causing authentication failures

| Field | Details |
|---|---|
| **ID** | BUG-002 |
| **Title** | Authentication token expires quickly causing 403 Forbidden on subsequent requests |
| **Module** | Auth |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | Open |
| **Environment** | Postman |

### Steps to Reproduce
1. Generate a valid authentication token via POST /auth
2. Wait a few minutes without executing any requests
3. Send PUT to /booking/{{bookingid}} with the previously generated token

### Expected Result
Request is authenticated successfully and booking is updated.

### Actual Result
Response status code is 403 Forbidden, indicating the token is no longer valid.

### Notes
The API does not document the token expiration time, which makes it difficult to plan test execution. A workaround is to regenerate the token immediately before executing authenticated requests.
