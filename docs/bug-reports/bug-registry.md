# Bug Reports Registry — Joom Project

This registry contains all defects identified during testing. Each report includes technical details necessary for reproduction and fixing

---

### BUG-01: Phone prefix not updating for Belarus
*   **ID:** BUG-01
*   **Summary:** Phone prefix does not update in the input field when "Belarus" is selected in the Country Selector
*   **Priority:** High
*   **Pre-conditions:** Registration page is open; default region is Russia (+7)
*   **Steps to reproduce:**
1. Open the country dropdown list
2. Select "Belarus"
3. Check the phone prefix value in the mobile number field.
*   **Actual Result:** Prefix remains `+7`.
*   **Expected Result:** Prefix automatically changes to `+375`
*   **Visual Proof:** [📸 View Screenshot](https://raw.githubusercontent.com/AlenaPetryk/joom-ecommerce-testing/refs/heads/bug-report-storage/chrome_Q8lXqAS0ix.png)

---

### BUG-02: Missing char limit warning in Profile Bio
*   **ID:** BUG-02
*   **Summary:** Absence of a warning message when exceeding the 2000-character limit in the "About Me" field
*   **Priority:** Medium
*   **Pre-conditions:** User is authorized; Profile Edit screen is open
*   **Steps to reproduce:**
1. Paste text with a length of 2000 characters into the "About Me" field
2. Click the "Save" button
*   **Actual Result:** Text is saved (truncated by the system); no error notification is displayed
*   **Expected Result:** A "Maximum characters" message is displayed, and the Save button is disabled
*   **Visual Proof:** [📸 View Screenshot](https://github.com/AlenaPetryk/joom-ecommerce-testing/blob/bug-report-storage/explorer_LSbmpjSZNq.png?raw=true)

---

### BUG-03: Empty search query validation failure
*   **ID:** BUG-03
*   **Summary:** Lack of validation and hints for search queries consisting only of spaces
*   **Priority:** Low
*   **Pre-conditions:** Main page is open
*   **Steps to reproduce:**
1. Enter 3 spaces into the search ba
2. Press Enter or click the Search icon
*   **Actual Result:** Page reloads, showing empty results without any warning
*   **Expected Result:** A validation hint "Please enter a keyword" appears
*   **Visual Proof:** [📸 View Screenshot](https://raw.githubusercontent.com/AlenaPetryk/joom-ecommerce-testing/refs/heads/bug-report-storage/3tcfcDWe8a.png)

---

### BUG-04: Category filter API error (iPhone SE)
*   **ID:** BUG-04
*   **Summary:** 400 Bad Request error when applying category filters in mobile emulation
*   **Priority:** High
*   **Pre-conditions:** Chrome browser; Device Mode (iPhone SE) activated
*   **Steps to reproduce:**
1. Open the product catalog
2. Select any category and apply any filter
*   **Actual Result:** Product list does not update; API error 400 is logged in the developer console
*   **Expected Result:** Product list is successfully filtered and updated in the UI
*   **Visual Proof:** [📸 View Screenshot](https://raw.githubusercontent.com/AlenaPetryk/joom-ecommerce-testing/refs/heads/bug-report-storage/chrome_gNWZfV2Gtr.png)

---

### BUG-5: Boundary price values bypass
*   **ID:** BUG-5
*   **Summary:** Ability to enter price values outside business-defined boundaries (9.99 and 10000.01)
*   **Priority:** Medium
*   **Pre-conditions:** "Price range" filter is open
*   **Steps to reproduce:**
1. Enter "9.99" in the "Min" field (**BVA**)
2. Enter "10000.01" in the "Max" field (**BVA**)
3. Apply the filter
*   **Actual Result:** Filter is applied with incorrect values
*   **Expected Result:** System automatically rounds/corrects values to allowed limits (10.00 and 10000.00)
*   **Visual Proof:** [📸 View Screenshot](https://raw.githubusercontent.com/AlenaPetryk/joom-ecommerce-testing/refs/heads/bug-report-storage/chrome_zBhNd2N6q4.png)

---

### BUG-6: Invalid ultra-low price range (0-1 ₽)
*   **ID:** BUG-6
*   **Summary:** System allows setting a price range from 0 to 1 Ruble without a warning
*   **Priority:** Low
*   **Pre-conditions:** Catalog is open; price filter is available
*   **Steps to reproduce:**
1. Set minimum price to 0 and maximum to 1 (**EP**)
2. Click "Apply"
*   **Actual Result:** Filter is accepted, showing "0 products"
*   **Expected Result:** A notification "Minimum price is 10" appears
*   **Visual Proof:** [📸 View Screenshot](https://raw.githubusercontent.com/AlenaPetryk/joom-ecommerce-testing/refs/heads/bug-report-storage/chrome_5hFNplzz4d.png)

---

### BUG-7: Non-sticky Header on scroll (Desktop)
*   **ID:** BUG-7
*   **Summary:** Site header is not fixed when scrolling down the page
*   **Priority:** Medium
*   **Pre-conditions:** Catalog page with many products
*   **Steps to reproduce:**
1. Scroll the page down by 500+ pixels
*   **Actual Result:** Header disappears from the viewport
*   **Expected Result:** Header remains fixed (sticky) at the top of the screen
*   **Visual Proof:** [📸 View Screenshot](https://github.com/AlenaPetryk/joom-ecommerce-testing/blob/bug-report-storage/lA5Ys263Vy.png?raw=true)

---

### BUG-8: Visual Layout Shift on load (iPhone SE)
*   **ID:** BUG-8
*   **Summary:** Significant UI element shift during banner loading in the mobile version
*   **Priority:** Medium
*   **Pre-conditions:** Chrome DevTools (iPhone SE); Network throttling: Fast 3G
*   **Steps to reproduce:**
1. Open the main page
2. Observe the position of category buttons while the main banner is loading
*   **Actual Result:** Elements "jump" down by 200px after the banner image appears
*   **Expected Result:** Space for the banner is reserved (skeleton/placeholder), preventing layout shift
*   **Visual Proof:** [📸 View Screenshot](https://raw.githubusercontent.com/AlenaPetryk/joom-ecommerce-testing/refs/heads/bug-report-storage/chrome_OstWxYT2m0.png)

---


