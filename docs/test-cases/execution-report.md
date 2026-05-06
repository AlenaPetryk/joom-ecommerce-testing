# 📂 Joom Project: Integrated Test Execution Report

## 📊 Summary
*   **Total Tests:** 33 | **Passed:** 25 | **Failed:** 8
*   **Environments:** Windows 11 (Chrome), iPhone SE Emulation (DevTools)

---

### 1. Registration & Auth


| ID | Type | Summary | Pre-conditions | Severity | Expected Result | Status | Bug-ID |
|:---|:---:|:---|:---|:---:|:---|:---:|:---:|
| **01** | **Pos** | Verify account registration with a valid email | Email not registered | **Critical** | Account created; confirmation shown | ✅ PASSED | **Bug-01**|
| **02** | **Neg** | Validate system response to invalid email format | Reg form opened | **Major** | Error: "Enter a valid email" | ✅ PASSED |
| **03** | **Neg** | Check mandatory email field validation | Password is filled | **Major** | Error: "Email is required" | ✅ PASSED |
| **04** | **Neg** | Validate password requirements (letters only) | Valid email entered | **Medium** | Error: "Password must contain letters" | ✅ PASSED |
| **05** | **Neg** | Check mandatory password field validation | Email is filled | **Major** | Error: "Password is required" | ✅ PASSED |
| **06** | **Pos** | Verify confirmation email delivery after signup | Form submitted | **Critical** | Confirmation email received | ✅ PASSED |
| **07** | **Pos** | Verify user authorization via VK Social OAuth | Valid VK account | **Major** | Successful login & data sync | ✅ PASSED |
| **08** | **Neg** | Check phone prefix update during Belarus selection | Country selector active | **Major** | Phone prefix updates to `+375` | ❌ FAILED | **Bug-02**|

### 2. Profile Management


| ID | Type | Summary | Pre-conditions | Severity | Expected Result | Status | **Bug-ID** |
|:---|:---:|:---|:---|:---:|:---|:---:|:---:|
| **09** | **Pos** | Verify successful update of About Me section | User is logged in | **Medium** | Data is saved and displayed | ✅ PASSED |
| **10** | **Neg** | Validate character limit for About Me input field | Profile edit mode | **Medium** | System shows char limit warning | ❌ FAILED | **Bug-03**|

### 3. Search & Filters


| ID | Type | Summary | Pre-conditions | Severity | Expected Result | Status | **Bug-ID**|
|:---|:---:|:---|:---|:---:|:---|:---:|:---:|
| **11** | **Pos** | Verify search results for full product name match | Main page loaded | **Major** | Product displayed as 1st result | ✅ PASSED |
| **12** | **Pos** | Check search suggestions visibility and relevance | Input field active | **Medium** | Dropdown shows hints (3+ chars) | ✅ PASSED |
| **13** | **Neg** | Validate system behavior for empty search query | Input contains spaces | **Low** | System shows "Enter keyword" hint | ❌ FAILED | **Bug-04**|
| **14** | **Neg** | Verify category filter functionality on iPhone SE | DevTools: iPhone SE | **Critical** | API returns correctly filtered data | ❌ FAILED | **Bug-05**|

### 4. Price & Catalog Logic (BVA/EP)


| ID | Type | Summary | Pre-conditions | Severity | Expected Result | Status |**Bug-ID** |
|:---|:---:|:---|:---|:---:|:---|:---:|:---:|
| **15** | **Pos** | Verify items filtering within valid price range (10.00/10000.00) | Catalog page opened | **Major** | Only items within range displayed | ✅ PASSED |
| **16** | **Neg** | Check price boundary validation for not valid values (9.99/10000.01) | Price inputs active | **Major** | System rejects values outside limits | ❌ FAILED | **Bug-05**
| **17** | **Neg** | Check system response to 0 input | Price inputs active | **Medium** | Error: "Min price is 10.00" | ❌ FAILED | **Bug-06**|
| **18** | Neg | Validate system response to special characters in price | Price inputs active | Low | Input is ignored or blocked | ✅ PASSED |

### 5. Shopping Cart & Payment


| ID | Type | Summary | Pre-conditions | Severity | Expected Result | Status | **Bug-ID** |
|:---|:---:|:---|:---|:---:|:---|:---:|:---:|
| **19** | **Pos** | Verify item quantity increment in the cart | Items in cart | **Major** | Total price updates instantly | ✅ PASSED |
| **20** | **Pos** | Check hover state smooth transition on Login button | Desktop env. | **Low** | Smooth color transition (0.3s) | ✅ PASSED |
| **21** | **Pos** | Verify burger menu tap area dimensions on mobile | DevTools: iPhone SE | **Major** | Tap area is at least 44x44px | ✅ PASSED |
| **22** | **Pos** | Check content alignment within mobile safe areas | DevTools: iPhone SE | **Major** | No overlap with notch/bottom bar | ✅ PASSED |
| **23** | **Neg** | Verify sticky behavior of the header on scroll | Long page loaded | **Low** | Header stays fixed on scroll | ❌ FAILED | **Bug-07**|
| **24** | **Neg** | Check for layout shift during page load | DevTools: iPhone SE | **Medium** | Elements don't "jump" on load | ❌ FAILED | **Bug-08**|

### 6. Promo Codes & Coupons


| ID | Type | Summary | Pre-conditions | Severity | Expected Result | Status |
|:---|:---:|:---|:---|:---:|:---|:---:|
| **25** | **Pos** | Verify discount application for first order promo | First purchase | **Major** | 10% discount is applied | ✅ PASSED |
| **26** | **Pos** | Verify brand-specific promo for multiple items | 2+ Uniqlo in cart | **Major** | 40% discount applied to Uniqlo | ✅ PASSED |
| **27** | **Neg** | Check promo code hint for insufficient item quantity | 1 Uniqlo in cart | **Medium** | Hint: "Add 1 more for discount" | ✅ PASSED |
| **28** | **Pos** | Verify discount for Sport category items | Sport items in cart | **Major** | 11% discount is applied | ✅ PASSED |
| **29** | **Neg** | Validate coupon stacking and priority logic | One coupon applied | **Medium** | System allows only one best coupon | ✅ PASSED |
| **30** | **Neg** | Check system trim for spaces in promo code field | Code with spaces | **Low** | Spaces trimmed and code applied | ✅ PASSED |
| **31** | **Neg** | Validate promo code input for invalid characters | Code field active | **Low** | Error: "Invalid promo code format" | ✅ PASSED |

### 7. Checkout & Final Order


| ID | Type | Summary | Pre-conditions | Severity | Expected Result | Status |
|:---|:---:|:---|:---|:---:|:---|:---:|
| **32** | **Pos** | Verify successful checkout and order placement | Valid payment; items | **Critical** | Order placed; email sent | ✅ PASSED |
| **33** | **Neg** | Check transaction rejection for expired credit card | Checkout page opened | **Critical** | Error shown; status: "Awaiting" | ✅ PASSED |
