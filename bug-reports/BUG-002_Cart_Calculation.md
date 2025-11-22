# BUG-002: Shopping Cart Total Calculation Incorrect

**Bug ID:** BUG-002  
**Title:** Shopping Cart Total Calculation Incorrect  
**Status:** Open  
**Date Reported:** November 16, 2024  
**Reported By:** Ayoub (QA Engineer)

---

## Summary

The shopping cart total calculation is incorrect. The tax is being calculated on the subtotal plus shipping, instead of just the subtotal.

---

## Description

When items are added to the cart, the total is calculated incorrectly. The system is applying tax to (subtotal + shipping), when it should only apply tax to the subtotal. This results in customers being overcharged.

---

## Steps to Reproduce

1. Log in to the application
2. Add a product priced at $100 to the cart
3. Select shipping method "Standard" ($10)
4. Observe the cart totals

---

## Expected Behavior

- Subtotal: $100.00
- Shipping: $10.00
- Tax (10%): $10.00 (calculated on subtotal only)
- **Total: $120.00**

---

## Actual Behavior

- Subtotal: $100.00
- Shipping: $10.00
- Tax (10%): $11.00 (calculated on subtotal + shipping)
- **Total: $121.00**

---

## Environment

| Property | Value |
| :--- | :--- |
| **Browser** | Chrome 120.0.0, Firefox 121.0 |
| **Operating System** | Windows 11, macOS 14 |
| **Environment** | Staging |
| **URL** | https://staging.ecommerce.local/cart |
| **Device** | Desktop |

---

## Severity

**Critical** - This is a financial issue affecting customer billing.

---

## Priority

**P1** - Must be fixed immediately.

---

## Root Cause Analysis

The tax calculation logic in the cart calculation function is incorrect. The formula is:
```
tax = (subtotal + shipping) * tax_rate
```

Should be:
```
tax = subtotal * tax_rate
```

---

## Suggested Solution

Update the cart calculation logic in the backend to calculate tax only on the subtotal, not including shipping costs.

**File to modify:** `/backend/services/cart_service.py`  
**Function:** `calculate_cart_totals()`

---

## Acceptance Criteria for Fix

- Tax is calculated only on subtotal
- Shipping is added after tax
- Total calculation is correct for all product combinations
- Tax calculation is correct for all tax rates
- Fix is verified with automated tests

---

## Attachments

- Screenshot: cart_calculation_error.png
- Test data: cart_test_cases.xlsx

---

## Related Issues

- None

---

## Comments

**Developer Response:** Confirmed the bug. Will fix in the next release.  
**QA Response:** This is a critical issue. Please provide ETA for fix.  
**Product Manager:** This affects customer trust. Fix should be prioritized.
