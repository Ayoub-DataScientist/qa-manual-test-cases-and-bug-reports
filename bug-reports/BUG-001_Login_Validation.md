# BUG-001: Login Form Accepts Invalid Email Format

**Bug ID:** BUG-001  
**Title:** Login Form Accepts Invalid Email Format  
**Status:** Open  
**Date Reported:** November 15, 2024  
**Reported By:** Ayoub (QA Engineer)

---

## Summary

The login form does not validate email format and accepts invalid emails, allowing form submission with malformed email addresses.

---

## Description

When entering an invalid email address in the login form (e.g., "invalid@", "user@", or "invalid"), the form does not display a validation error and allows the user to submit the form. This results in a server-side error instead of client-side validation.

---

## Steps to Reproduce

1. Navigate to https://demo.ecommerce.local/login
2. Enter email: "invalid@"
3. Enter password: "password123"
4. Click "Sign In" button
5. Observe the response

---

## Expected Behavior

- Form should display client-side validation error message: "Please enter a valid email address"
- Submit button should be disabled until a valid email is entered
- Form submission should be prevented
- User should remain on the login page

---

## Actual Behavior

- No validation error is displayed on the client side
- Form is submitted with invalid email
- Server returns 400 Bad Request error after submission
- User sees a generic error message: "Invalid request"

---

## Environment

| Property | Value |
| :--- | :--- |
| **Browser** | Chrome 120.0.0 |
| **Operating System** | Windows 11 |
| **Environment** | Staging |
| **URL** | https://staging.ecommerce.local/login |
| **Device** | Desktop |

---

## Severity

**High** - This affects user experience and allows invalid data submission.

---

## Priority

**P2** - Should be fixed in the current sprint.

---

## Root Cause Analysis

The login form is missing client-side email validation using HTML5 input type="email" or JavaScript validation before form submission.

---

## Suggested Solution

Implement client-side email validation using one of the following approaches:
1. Use HTML5 `<input type="email">` with validation
2. Implement JavaScript regex validation for email format
3. Use a validation library like Validator.js

---

## Acceptance Criteria for Fix

- Email field rejects invalid formats before form submission
- Clear error message is displayed for invalid email
- Valid email formats are accepted
- Form submission is prevented for invalid emails

---

## Attachments

- Screenshot: invalid_email_error.png
- Console logs: browser_console.log

---

## Related Issues

- Similar validation issue reported for password field (BUG-002)

---

## Comments

**Developer Response:** Will implement HTML5 email validation in the next update.  
**QA Response:** Please ensure validation works across all browsers.
