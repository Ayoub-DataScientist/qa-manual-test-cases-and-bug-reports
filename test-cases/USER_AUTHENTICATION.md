# Test Cases: User Authentication

## TC-001: Valid User Login

**Test Case ID:** TC-001  
**Title:** Valid User Login  
**Description:** Verify that a user can successfully log in with valid credentials.

**Preconditions:**
- User account exists with email: testuser@example.com
- Password: TestPassword123!
- User is not currently logged in
- Application is accessible

**Steps:**
1. Navigate to the login page
2. Enter email: testuser@example.com
3. Enter password: TestPassword123!
4. Click "Sign In" button
5. Wait for page to load

**Expected Result:**
- User is successfully authenticated
- User is redirected to the dashboard
- Welcome message displays user's name
- Session is created

**Priority:** Critical  
**Severity:** Critical  
**Status:** Pass

---

## TC-002: Invalid Email Login

**Test Case ID:** TC-002  
**Title:** Invalid Email Login  
**Description:** Verify that login fails with an invalid email address.

**Preconditions:**
- User is not currently logged in
- Application is accessible

**Steps:**
1. Navigate to the login page
2. Enter email: invalid@example.com
3. Enter password: TestPassword123!
4. Click "Sign In" button
5. Wait for response

**Expected Result:**
- Login fails
- Error message displays: "Invalid credentials"
- User remains on login page
- No session is created

**Priority:** Critical  
**Severity:** Critical  
**Status:** Pass

---

## TC-003: Invalid Password Login

**Test Case ID:** TC-003  
**Title:** Invalid Password Login  
**Description:** Verify that login fails with an incorrect password.

**Preconditions:**
- User account exists with email: testuser@example.com
- User is not currently logged in
- Application is accessible

**Steps:**
1. Navigate to the login page
2. Enter email: testuser@example.com
3. Enter password: WrongPassword123!
4. Click "Sign In" button
5. Wait for response

**Expected Result:**
- Login fails
- Error message displays: "Invalid credentials"
- User remains on login page
- No session is created

**Priority:** Critical  
**Severity:** Critical  
**Status:** Pass

---

## TC-004: Empty Email Field

**Test Case ID:** TC-004  
**Title:** Empty Email Field  
**Description:** Verify that login fails when email field is empty.

**Preconditions:**
- User is not currently logged in
- Application is accessible

**Steps:**
1. Navigate to the login page
2. Leave email field empty
3. Enter password: TestPassword123!
4. Click "Sign In" button

**Expected Result:**
- Form validation error displays
- Error message: "Email is required"
- Submit button is disabled or form is not submitted
- User remains on login page

**Priority:** High  
**Severity:** High  
**Status:** Pass

---

## TC-005: Empty Password Field

**Test Case ID:** TC-005  
**Title:** Empty Password Field  
**Description:** Verify that login fails when password field is empty.

**Preconditions:**
- User is not currently logged in
- Application is accessible

**Steps:**
1. Navigate to the login page
2. Enter email: testuser@example.com
3. Leave password field empty
4. Click "Sign In" button

**Expected Result:**
- Form validation error displays
- Error message: "Password is required"
- Submit button is disabled or form is not submitted
- User remains on login page

**Priority:** High  
**Severity:** High  
**Status:** Pass

---

## TC-006: User Registration

**Test Case ID:** TC-006  
**Title:** User Registration  
**Description:** Verify that a new user can register an account.

**Preconditions:**
- User is not currently logged in
- Email newuser@example.com is not registered
- Application is accessible

**Steps:**
1. Navigate to the login page
2. Click "Create Account" link
3. Enter email: newuser@example.com
4. Enter password: NewPassword123!
5. Confirm password: NewPassword123!
6. Click "Register" button
7. Wait for confirmation

**Expected Result:**
- Account is created successfully
- Confirmation message displays
- User is redirected to login page or dashboard
- User can log in with new credentials

**Priority:** Critical  
**Severity:** Critical  
**Status:** Pass

---

## TC-007: Password Reset

**Test Case ID:** TC-007  
**Title:** Password Reset  
**Description:** Verify that a user can reset their password.

**Preconditions:**
- User account exists with email: testuser@example.com
- User is not currently logged in
- Application is accessible

**Steps:**
1. Navigate to the login page
2. Click "Forgot Password" link
3. Enter email: testuser@example.com
4. Click "Send Reset Link" button
5. Check email for reset link
6. Click reset link in email
7. Enter new password: NewPassword456!
8. Confirm password: NewPassword456!
9. Click "Reset Password" button

**Expected Result:**
- Password reset email is sent
- Reset link is valid and works
- Password is updated successfully
- User can log in with new password
- Old password no longer works

**Priority:** High  
**Severity:** High  
**Status:** Pass

---

## TC-008: Session Persistence

**Test Case ID:** TC-008  
**Title:** Session Persistence  
**Description:** Verify that user session persists across page navigation.

**Preconditions:**
- User is logged in
- Session is active

**Steps:**
1. User is on dashboard
2. Navigate to Products page
3. Navigate to Cart page
4. Navigate back to Dashboard
5. Refresh the page

**Expected Result:**
- User remains logged in throughout navigation
- Session is not lost
- User information is accessible on all pages
- No re-login is required

**Priority:** High  
**Severity:** High  
**Status:** Pass

---

## TC-009: User Logout

**Test Case ID:** TC-009  
**Title:** User Logout  
**Description:** Verify that a user can log out and session is destroyed.

**Preconditions:**
- User is logged in
- Session is active

**Steps:**
1. Click "Logout" button
2. Wait for page to load
3. Attempt to access dashboard without logging in

**Expected Result:**
- User is logged out successfully
- User is redirected to login page
- Session is destroyed
- User cannot access protected pages without logging in

**Priority:** High  
**Severity:** High  
**Status:** Pass

---

## TC-010: Case-Insensitive Email

**Test Case ID:** TC-010  
**Title:** Case-Insensitive Email  
**Description:** Verify that email login is case-insensitive.

**Preconditions:**
- User account exists with email: testuser@example.com
- User is not currently logged in

**Steps:**
1. Navigate to the login page
2. Enter email: TESTUSER@EXAMPLE.COM
3. Enter password: TestPassword123!
4. Click "Sign In" button

**Expected Result:**
- Login succeeds
- Email is treated as case-insensitive
- User is redirected to dashboard
- Session is created

**Priority:** Medium  
**Severity:** Medium  
**Status:** Pass
