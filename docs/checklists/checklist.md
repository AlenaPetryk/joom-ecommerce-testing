# ✅ Joom Regression Checklist (Traceability Version)

This checklist is linked to the [Test Execution Report](../test-cases/execution-report.md) for detailed verification steps.

---

## 1. 🔑 Registration & Auth
- [ ] **REG-01**: Successful account creation with a valid email. `(TC-01, TC-06)`
- [ ] **REG-02**: Email field validation (invalid format and empty input). `(TC-02, TC-03)`
- [ ] **REG-03**: Password field validation (mandatory status and letters requirement). `(TC-04, TC-05)`
- [ ] **REG-04**: Social authorization via VK OAuth. `(TC-07)`
- [ ] **REG-05**: Phone prefix update for Belarus selection (+375). `(TC-08)`

## 2. 👤 Profile Management
- [ ] **PRO-01**: Successful "About Me" section update. `(TC-09)`
- [ ] **PRO-02**: Character limit enforcement for the "About Me" field. `(TC-10)`

## 3. 🔍 Search & Filters
- [ ] **SRH-01**: Product search by full name and suggestions visibility. `(TC-11, TC-12)`
- [ ] **SRH-02**: Validation for empty search queries (spaces). `(TC-13)`
- [ ] **CAT-01**: Mobile-specific category filter functionality. `(TC-14)`

## 4. 📊 Price & Catalog Logic
- [ ] **CAT-02**: Valid price range filtering (10.00 / 10000.00). `(TC-15)`
- [ ] **CAT-03**: Price boundary validation (9.99 / 10,000.01). `(TC-16)`
- [ ] **CAT-04**: Handling of zero price and ultra-low ranges (0-1 ₽). `(TC-17)`
- [ ] **CAT-05**: Sanitization of special characters in price fields. `(TC-18)`

## 5. 🛒 Shopping Cart & Payment
- [ ] **CRT-01**: Quantity increment via "+" with instant price recalculation. `(TC-19)`
- [ ] **CRT-02**: Hover states for interactive UI elements. `(TC-20)`
- [ ] **PAY-01**: Rejection of expired credit card transactions. `(TC-33)`

## 6. 🏷️ Promo Codes & Coupons
- [ ] **CPN-01**: First order and Uniqlo (2+ items) discount application. `(TC-25, TC-26)`
- [ ] **CPN-02**: Hint display for partially met promo conditions. `(TC-27)`
- [ ] **CPN-03**: Sport category promo and coupon stacking logic. `(TC-28, TC-29)`
- [ ] **CPN-04**: Promo code field: special characters validation. `(TC-30, TC-31)`

## 7. 📱 UI/UX & Mobile Adaptation (iPhone SE)
- [ ] **UI-01**: Burger menu tap area size (min 44x44px). `(TC-21)`
- [ ] **UI-02**: Safe Area alignment (Notch/Bottom bar). `(TC-22)`
- [ ] **UI-03**: Sticky header behavior during scroll. `(TC-23)`
- [ ] **UI-04**: Cumulative Layout Shift (CLS) check during load. `(TC-24)`

## 💳 Checkout & Final Order
- [ ] **ORD-01**: Complete End-to-End order placement flow. `(TC-32)`
