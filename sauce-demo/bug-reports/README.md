# Bug Reports — Sauce Demo

## BUG-001 — Locked out user receives generic error message

| Field | Details |
|---|---|
| **ID** | BUG-001 |
| **Title** | Locked out user receives generic error message |
| **Module** | Login |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | Open |
| **Environment** | Chromium, Firefox, WebKit |

### Steps to Reproduce
1. Go to https://www.saucedemo.com
2. Enter username: `locked_out_user`
3. Enter password: `secret_sauce`
4. Click Login

### Expected Result
A specific message informing the user that their account has been locked and to contact support.

### Actual Result
A generic error message is displayed: *"Epic sadface: Sorry, this user has been locked out."*

### Notes
The error message does not provide actionable guidance to the user, such as a contact email or support link.

---

## BUG-002 — Problem user displays broken product images

| Field | Details |
|---|---|
| **ID** | BUG-002 |
| **Title** | Problem user displays broken product images |
| **Module** | Inventory |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |
| **Environment** | Chromium, Firefox, WebKit |

### Steps to Reproduce
1. Go to https://www.saucedemo.com
2. Enter username: `problem_user`
3. Enter password: `secret_sauce`
4. Click Login
5. Observe the product list

### Expected Result
All product images are displayed correctly.

### Actual Result
All product images are broken — the same placeholder image is displayed for every product.

### Notes
This issue affects the entire inventory page for the problem_user account and would prevent users from visually identifying products.

---

## BUG-003 — Problem user cannot sort products

| Field | Details |
|---|---|
| **ID** | BUG-003 |
| **Title** | Problem user cannot sort products |
| **Module** | Inventory |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |
| **Environment** | Chromium, Firefox, WebKit |

### Steps to Reproduce
1. Go to https://www.saucedemo.com
2. Log in as `problem_user`
3. Click the sort dropdown
4. Select any sort option

### Expected Result
Products are sorted according to the selected option.

### Actual Result
Products remain in the original order regardless of the sort option selected.

### Notes
This issue is specific to the problem_user account and does not affect standard_user.
