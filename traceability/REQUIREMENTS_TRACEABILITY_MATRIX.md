# Requirements Traceability Matrix (RTM)

**Project:** Ecommerce Platform  
**Version:** 1.0  
**Date:** November 2024  
**Prepared By:** Ayoub (QA Lead)

---

## Purpose

This traceability matrix maps each requirement to its corresponding test cases, ensuring complete test coverage and accountability.

---

## Traceability Matrix

| Req ID | Requirement | Test Case ID | Test Case Title | Status | Coverage |
| :--- | :--- | :--- | :--- | :--- | :--- |
| REQ-001 | User can log in with valid credentials | TC-001 | Valid User Login | ✓ Pass | Positive |
| REQ-001 | User can log in with valid credentials | TC-002 | Invalid Email Login | ✓ Pass | Negative |
| REQ-001 | User can log in with valid credentials | TC-003 | Invalid Password Login | ✓ Pass | Negative |
| REQ-001 | User can log in with valid credentials | TC-004 | Empty Email Field | ✓ Pass | Negative |
| REQ-001 | User can log in with valid credentials | TC-005 | Empty Password Field | ✓ Pass | Negative |
| REQ-001 | User can log in with valid credentials | TC-010 | Case-Insensitive Email | ✓ Pass | Edge Case |
| REQ-001 | User can register new account | TC-006 | User Registration | ✓ Pass | Positive |
| REQ-001 | User can reset password | TC-007 | Password Reset | ✓ Pass | Positive |
| REQ-001 | Session persists across navigation | TC-008 | Session Persistence | ✓ Pass | Functional |
| REQ-001 | User can log out | TC-009 | User Logout | ✓ Pass | Positive |
| REQ-002 | User can search for products | TC-011 | Search Existing Product | ✓ Pass | Positive |
| REQ-002 | User can search for products | TC-012 | Search Non-Existent Product | ✓ Pass | Negative |
| REQ-002 | User can filter by category | TC-013 | Filter by Category | ✓ Pass | Positive |
| REQ-002 | User can filter by price range | TC-014 | Filter by Price Range | ✓ Pass | Positive |
| REQ-002 | User can sort products | TC-015 | Sort by Price (Low-High) | ✓ Pass | Positive |
| REQ-002 | User can sort products | TC-016 | Sort by Price (High-Low) | ✓ Pass | Positive |
| REQ-002 | User can sort products | TC-017 | Sort by Rating | ✓ Pass | Positive |
| REQ-003 | User can add items to cart | TC-020 | Add Product to Cart | ✓ Pass | Positive |
| REQ-003 | User can update item quantities | TC-021 | Update Item Quantity | ✓ Pass | Positive |
| REQ-003 | User can remove items from cart | TC-022 | Remove Item from Cart | ✓ Pass | Positive |
| REQ-003 | Cart displays correct totals | TC-023 | Cart Totals Calculation | ✓ Pass | Functional |
| REQ-003 | Cart persists across sessions | TC-024 | Cart Persistence | ✓ Pass | Functional |
| REQ-004 | User can complete checkout | TC-030 | Complete Checkout | ✓ Pass | Positive |
| REQ-004 | Form validates required fields | TC-031 | Checkout Missing First Name | ✓ Pass | Negative |
| REQ-004 | Form validates email format | TC-032 | Checkout Invalid Email | ✓ Pass | Negative |
| REQ-004 | Form validates phone format | TC-033 | Checkout Invalid Phone | ✓ Pass | Negative |
| REQ-004 | Payment is processed securely | TC-034 | Checkout Valid Payment | ✓ Pass | Positive |
| REQ-004 | User receives order confirmation | TC-035 | Order Confirmation Email | ✓ Pass | Functional |
| REQ-005 | User can view profile | TC-040 | View User Profile | ✓ Pass | Positive |
| REQ-005 | User can update email | TC-041 | Update Email Address | ✓ Pass | Positive |
| REQ-005 | User can update password | TC-042 | Update Password | ✓ Pass | Positive |
| REQ-005 | User can view order history | TC-043 | View Order History | ✓ Pass | Positive |

---

## Coverage Summary

| Requirement | Total Test Cases | Passed | Failed | Blocked | Coverage % |
| :--- | :--- | :--- | :--- | :--- | :--- |
| REQ-001: Authentication | 10 | 10 | 0 | 0 | 100% |
| REQ-002: Product Catalog | 7 | 7 | 0 | 0 | 100% |
| REQ-003: Shopping Cart | 5 | 5 | 0 | 0 | 100% |
| REQ-004: Checkout & Payment | 6 | 6 | 0 | 0 | 100% |
| REQ-005: User Profile | 4 | 4 | 0 | 0 | 100% |
| **TOTAL** | **32** | **32** | **0** | **0** | **100%** |

---

## Test Coverage by Type

| Test Type | Count | Percentage |
| :--- | :--- | :--- |
| Positive Tests | 18 | 56% |
| Negative Tests | 10 | 31% |
| Edge Cases | 2 | 6% |
| Functional Tests | 2 | 6% |

---

## Untested Requirements

None - all requirements have corresponding test cases.

---

## Sign-Off

| Role | Name | Date | Signature |
| :--- | :--- | :--- | :--- |
| QA Lead | Ayoub | Nov 20, 2024 | ✓ |
| Development Lead | Michael Chen | Nov 20, 2024 | ✓ |
| Product Owner | Sarah Johnson | Nov 20, 2024 | ✓ |
