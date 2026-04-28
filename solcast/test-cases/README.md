# Test Cases — Solcast Website

## Navigation

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-001 | Homepage loads successfully | Website is accessible | 1. Go to https://solcast.com.br | Page loads and URL is https://solcast.com.br/ | ✅ Pass |
| TC-002 | Navigate to Sobre nós page | Website is accessible | 1. Go to https://solcast.com.br 2. Click Sobre nós in the menu | User is redirected to /sobre-nos/ | ✅ Pass |
| TC-003 | Navigate to Serviços page | Website is accessible | 1. Go to https://solcast.com.br 2. Click Serviços in the menu | User is redirected to /servicos/ | ✅ Pass |
| TC-004 | Navigate to Cases page | Website is accessible | 1. Go to https://solcast.com.br 2. Click Cases in the menu | User is redirected to /cases/ | ✅ Pass |
| TC-005 | Navigate to Contato page | Website is accessible | 1. Go to https://solcast.com.br 2. Click Contato in the menu | User is redirected to /contato/ | ✅ Pass |

---

## Homepage

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-006 | Display company logo | Website is accessible | 1. Go to https://solcast.com.br 2. Observe the header | Company logo is visible | ✅ Pass |
| TC-007 | Display main headline | Website is accessible | 1. Go to https://solcast.com.br 2. Observe the first section | Main headline text is visible | ✅ Pass |
| TC-008 | Display services link | Website is accessible | 1. Go to https://solcast.com.br 2. Observe the page | Services section link is visible | ✅ Pass |
| TC-009 | Display cases link | Website is accessible | 1. Go to https://solcast.com.br 2. Observe the page | Cases section link is visible | ✅ Pass |
| TC-010 | Display budget button | Website is accessible | 1. Go to https://solcast.com.br 2. Observe the header | Budget button is visible | ✅ Pass |
| TC-011 | Display contact information | Website is accessible | 1. Go to https://solcast.com.br 2. Scroll to the contact section | Contact email is visible | ✅ Pass |

---

## Contact Form

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-012 | Display contact form | Website is accessible | 1. Go to https://solcast.com.br/contato/ 2. Observe the page | All form fields and submit button are visible | ✅ Pass |
| TC-013 | Accept input in name field | Website is accessible | 1. Go to https://solcast.com.br/contato/ 2. Type a name in the Nome field | Field accepts and displays the typed value | ✅ Pass |
| TC-014 | Accept input in phone field | Website is accessible | 1. Go to https://solcast.com.br/contato/ 2. Type a phone number in the Telefone field | Field accepts and displays the typed value | ✅ Pass |
| TC-015 | Accept input in email field | Website is accessible | 1. Go to https://solcast.com.br/contato/ 2. Type an email in the E-mail field | Field accepts and displays the typed value | ✅ Pass |
| TC-016 | Accept input in message field | Website is accessible | 1. Go to https://solcast.com.br/contato/ 2. Type a message in the Mensagem field | Field accepts and displays the typed value | ✅ Pass |

---

## Responsive

| ID | Title | Preconditions | Steps | Expected Result | Status |
|---|---|---|---|---|---|
| TC-017 | Display hamburger menu on mobile | Website is accessible | 1. Set viewport to 375x812 2. Go to https://solcast.com.br 3. Observe the header | Hamburger menu icon is visible | ✅ Pass |
| TC-018 | Display budget button on mobile | Website is accessible | 1. Set viewport to 375x812 2. Go to https://solcast.com.br 3. Observe the header | Budget button is visible | ✅ Pass |
| TC-019 | Display logo on mobile | Website is accessible | 1. Set viewport to 375x812 2. Go to https://solcast.com.br 3. Observe the header | Company logo is visible | ✅ Pass |
| TC-020 | Display desktop menu | Website is accessible | 1. Set viewport to 1280x800 2. Go to https://solcast.com.br 3. Observe the header | Full navigation menu is visible | ✅ Pass |
| TC-021 | Display logo on desktop | Website is accessible | 1. Set viewport to 1280x800 2. Go to https://solcast.com.br 3. Observe the header | Company logo is visible | ✅ Pass |
