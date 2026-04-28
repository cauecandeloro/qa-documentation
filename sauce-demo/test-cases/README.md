# Test Cases — Sauce Demo

## Login

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-001 | Login with valid credentials | Application is accessible | 1. Go to https://www.saucedemo.com 2. Enter username: standard_user 3. Enter password: secret_sauce 4. Click Login | User is redirected to /inventory.html | ✅ Pass |
| TC-002 | Login with invalid credentials | Application is accessible | 1. Go to https://www.saucedemo.com 2. Enter username: invalid_user 3. Enter password: wrong_password 4. Click Login | Error message is displayed | ✅ Pass |
| TC-003 | Login with empty fields | Application is accessible | 1. Go to https://www.saucedemo.com 2. Click Login without filling any field | Error message is displayed | ✅ Pass |

---

## Inventory

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-004 | Display product list | User is logged in | 1. Log in as standard_user 2. Observe the inventory page | 6 products are displayed | ✅ Pass |
| TC-005 | Sort products by name A to Z | User is logged in | 1. Log in as standard_user 2. Select sort option A to Z | First product is Sauce Labs Backpack | ✅ Pass |
| TC-006 | Sort products by name Z to A | User is logged in | 1. Log in as standard_user 2. Select sort option Z to A | First product is Test.allTheThings() T-Shirt | ✅ Pass |
| TC-007 | Sort products by price low to high | User is logged in | 1. Log in as standard_user 2. Select sort option Low to High | First product is Sauce Labs Onesie | ✅ Pass |
| TC-008 | Sort products by price high to low | User is logged in | 1. Log in as standard_user 2. Select sort option High to Low | First product is Sauce Labs Fleece Jacket | ✅ Pass |
| TC-009 | Navigate to product detail | User is logged in | 1. Log in as standard_user 2. Click on a product title | Product detail page is displayed | ✅ Pass |

---

## Cart

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-010 | Add product to cart | User is logged in | 1. Log in as standard_user 2. Click Add to cart on Sauce Labs Backpack 3. Click cart icon | Product is displayed in cart | ✅ Pass |
| TC-011 | Remove product from cart | User is logged in | 1. Log in as standard_user 2. Add Sauce Labs Backpack to cart 3. Go to cart 4. Click Remove | Cart is empty | ✅ Pass |
| TC-012 | Cart badge updates on add | User is logged in | 1. Log in as standard_user 2. Click Add to cart on Sauce Labs Backpack | Cart badge displays 1 | ✅ Pass |
| TC-013 | Add multiple products to cart | User is logged in | 1. Log in as standard_user 2. Add Sauce Labs Backpack 3. Add Sauce Labs Bike Light 4. Go to cart | 2 products are displayed in cart | ✅ Pass |

---

## Checkout

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-014 | Complete checkout with valid information | Product added to cart | 1. Go to cart 2. Click Checkout 3. Fill First Name, Last Name and Postal Code 4. Click Continue 5. Click Finish | Order confirmation message is displayed | ✅ Pass |
| TC-015 | Checkout without first name | Product added to cart | 1. Go to cart 2. Click Checkout 3. Fill only Last Name and Postal Code 4. Click Continue | Error message is displayed | ✅ Pass |
| TC-016 | Checkout without last name | Product added to cart | 1. Go to cart 2. Click Checkout 3. Fill only First Name and Postal Code 4. Click Continue | Error message is displayed | ✅ Pass |
| TC-017 | Checkout without postal code | Product added to cart | 1. Go to cart 2. Click Checkout 3. Fill only First Name and Last Name 4. Click Continue | Error message is displayed | ✅ Pass |
| TC-018 | Order summary before finishing | Product added to cart | 1. Go to cart 2. Click Checkout 3. Fill all fields 4. Click Continue | Product and total price are displayed | ✅ Pass |

---

## Logout

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-019 | Logout successfully | User is logged in | 1. Log in as standard_user 2. Click burger menu 3. Click Logout | User is redirected to login page | ✅ Pass |
| TC-020 | Access inventory after logout | User is logged out | 1. Log out 2. Navigate to /inventory.html | User is redirected to login page | ✅ Pass |
