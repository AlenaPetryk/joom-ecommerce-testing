# ✅ Joom Regression Checklist (Traceability Version)


---

## 1. 🔑 Registration & Auth
- [ ] **REG-01**: Successful account creation with a valid email. 
- [ ] **REG-02**: Email field validation (invalid format and empty input). 
- [ ] **REG-03**: Password field validation (mandatory status and letters requirement).
- [ ] **REG-04**: Social authorization via VK OAuth. `(TC-07)`
- [ ] **REG-05**: Phone prefix update for Belarus selection (+375).

## 2. 👤 Profile Management
- [ ] **PRO-01**: Successful "About Me" section update. 
- [ ] **PRO-02**: Character limit enforcement for the "About Me" field. 

## 3. 🔍 Search & Filters
- [ ] **SRH-01**: Product search by full name and suggestions visibility. 
- [ ] **SRH-02**: Validation for empty search queries (spaces). 
- [ ] **CAT-01**: Mobile-specific category filter functionality. 

## 4. 📊 Price & Catalog Logic
- [ ] **CAT-02**: Valid price range filtering (10.00 / 10000.00). 
- [ ] **CAT-03**: Price boundary validation (9.99 / 10,000.01). 
- [ ] **CAT-04**: Handling of zero price and ultra-low ranges (0-1 ₽).
- [ ] **CAT-05**: Sanitization of special characters in price fields. 

## 5. 🛒 Shopping Cart & Payment
- [ ] **CRT-01**: Quantity increment via "+" with instant price recalculation. 
- [ ] **CRT-02**: Hover states for interactive UI elements.
- [ ] **PAY-01**: Rejection of expired credit card transactions.

## 6. 🏷️ Promo Codes & Coupons
- [ ] **CPN-01**: First order and Uniqlo (2+ items) discount application. 
- [ ] **CPN-02**: Hint display for partially met promo conditions.`
- [ ] **CPN-03**: Sport category promo and coupon stacking logic. 
- [ ] **CPN-04**: Promo code field: special characters validation. 

## 7. 📱 UI/UX & Mobile Adaptation (iPhone SE)
- [ ] **UI-01**: Burger menu tap area size (min 44x44px). 
- [ ] **UI-02**: Safe Area alignment (Notch/Bottom bar). 
- [ ] **UI-03**: Sticky header behavior during scroll. 
- [ ] **UI-04**: Cumulative Layout Shift (CLS) check during load.

## 💳 Checkout & Final Order
- [ ] **ORD-01**: Complete End-to-End order placement flow. 
