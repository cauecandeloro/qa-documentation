# Bug Reports — Solcast Website

## BUG-001 — Cookie consent banner may overlap page content on mobile

| Field | Details |
|---|---|
| **ID** | BUG-001 |
| **Title** | Cookie consent banner may overlap page content on mobile viewport |
| **Module** | Homepage |
| **Severity** | Low |
| **Priority** | Low |
| **Status** | Open |
| **Environment** | Chromium — Mobile viewport 375x812 |

### Steps to Reproduce
1. Open https://solcast.com.br on a mobile viewport (375x812)
2. Observe the cookie consent banner position
3. Attempt to interact with page content below the banner

### Expected Result
Cookie consent banner is displayed without overlapping interactive page content, or is dismissible before content interaction.

### Actual Result
The cookie consent banner occupies a significant portion of the screen on mobile viewports, potentially overlapping calls to action and navigation elements before the user dismisses it.

### Notes
This issue does not affect desktop viewports. Automated tests handle this by running after page load, but real users on first visit may experience reduced usability until the banner is dismissed.

---

## BUG-002 — Menu items with special characters cause selector instability in automation

| Field | Details |
|---|---|
| **ID** | BUG-002 |
| **Title** | Menu items with special characters cause selector instability in automation |
| **Module** | Navigation |
| **Severity** | Low |
| **Priority** | Medium |
| **Status** | Resolved |
| **Environment** | Chromium, Firefox, WebKit |

### Steps to Reproduce
1. Attempt to locate the Serviços menu item using text-based selector: text=Serviços
2. Execute the automated test

### Expected Result
Selector finds the element and the test passes.

### Actual Result
Selector fails with timeout error due to special character ç not being recognized correctly.

### Resolution
Selector was updated to use href-based approach: a[href*="servicos"] — which resolves the special character issue and improves selector robustness.

### Notes
Menu items containing accented characters (ç, ã, é, etc.) should be targeted using attribute-based selectors rather than text-based selectors in Playwright to ensure cross-browser stability.
