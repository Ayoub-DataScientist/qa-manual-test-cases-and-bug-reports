# Manual QA Test Cases & Professional Bug Reports

##  Project Overview

This repository demonstrates **professional manual QA practices** including **test case design**, **bug reporting**, **requirements analysis**, and **test traceability**. It showcases how to document QA work in a professional manner that aligns with industry standards and JIRA conventions.

**QA Skills Demonstrated:**
- Writing clear, detailed test cases with expected results
- Documenting bugs in JIRA-style format with all necessary information
- Creating requirements documents and traceability matrices
- Organizing test cases by feature and priority
- Professional communication of quality issues

---

##  Contents

This repository contains:

1. **Test Cases** - Comprehensive manual test cases organized by feature
2. **Bug Reports** - Professional bug reports in JIRA-style format
3. **Requirements Document** - Sample product requirements with acceptance criteria
4. **Traceability Matrix** - Mapping requirements to test cases

---

##  Project Structure

```
qa-manual-test-cases-and-bug-reports/
├── README.md                          # This file
├── REQUIREMENTS.md                    # Product requirements document
├── test-cases/                        # Manual test cases
│   ├── USER_AUTHENTICATION.md         # Login/registration test cases
│   ├── PRODUCT_MANAGEMENT.md          # Product search/filtering test cases
│   ├── SHOPPING_CART.md               # Cart operations test cases
│   ├── CHECKOUT_PAYMENT.md            # Checkout and payment test cases
│   └── USER_PROFILE.md                # User profile management test cases
├── bug-reports/                       # Professional bug reports
│   ├── BUG-001_Login_Validation.md
│   ├── BUG-002_Cart_Calculation.md
│   ├── BUG-003_Search_Performance.md
│   ├── BUG-004_Payment_Error.md
│   └── BUG-005_UI_Alignment.md
├── traceability/                      # Traceability documents
│   ├── REQUIREMENTS_TRACEABILITY_MATRIX.md
│   └── TEST_COVERAGE_SUMMARY.md
└── templates/                         # Reusable templates
    ├── TEST_CASE_TEMPLATE.md
    └── BUG_REPORT_TEMPLATE.md
```

---

##  Getting Started

### Prerequisites
- Markdown editor or viewer
- Basic familiarity with QA terminology
- Understanding of JIRA or similar issue tracking systems

### How to Use This Repository

1. **Review Test Cases:** Navigate to the `test-cases/` folder to see how professional test cases are written.
2. **Study Bug Reports:** Check the `bug-reports/` folder for examples of well-documented bugs.
3. **Understand Requirements:** Read `REQUIREMENTS.md` to see how requirements are structured.
4. **Check Traceability:** Review the traceability matrix to understand how requirements map to tests.
5. **Use Templates:** Copy templates from the `templates/` folder for your own documentation.

---

##  Test Case Format

Each test case includes:
- **Test Case ID:** Unique identifier (e.g., TC-001)
- **Title:** Clear, descriptive name
- **Description:** What is being tested
- **Preconditions:** Setup required before the test
- **Steps:** Numbered, detailed action steps
- **Expected Result:** What should happen
- **Actual Result:** What actually happened (filled during execution)
- **Status:** Pass/Fail/Blocked
- **Priority:** Critical/High/Medium/Low
- **Severity:** Critical/High/Medium/Low

### Example Test Case

```markdown
## TC-001: Valid User Login

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
```

---

##  Bug Report Format

Each bug report includes:
- **Bug ID:** Unique identifier (e.g., BUG-001)
- **Title:** Clear, concise summary
- **Description:** Detailed explanation of the issue
- **Steps to Reproduce:** Exact steps to trigger the bug
- **Expected Behavior:** What should happen
- **Actual Behavior:** What actually happens
- **Severity:** Critical/High/Medium/Low
- **Priority:** P1/P2/P3/P4
- **Environment:** Where the bug was found
- **Attachments:** Screenshots, logs, etc.
- **Assigned To:** Developer responsible for the fix

### Example Bug Report

```markdown
## BUG-001: Login Form Accepts Invalid Email Format

**Summary:** The login form does not validate email format and accepts invalid emails.

**Description:** 
When entering an invalid email address in the login form (e.g., "invalid@"), the form 
does not display a validation error and allows the user to submit the form.

**Steps to Reproduce:**
1. Navigate to login page
2. Enter email: "invalid@"
3. Enter password: "password123"
4. Click "Sign In"

**Expected Behavior:**
- Form should display error message: "Please enter a valid email address"
- Submit button should be disabled or form submission should be prevented

**Actual Behavior:**
- No validation error is displayed
- Form is submitted with invalid email
- Server returns 400 error after submission

**Severity:** High
**Priority:** P2
**Environment:** Chrome 120.0, Windows 11, Staging
**Status:** Open
**Assigned To:** Backend Team
```

---

##  Traceability Matrix

The traceability matrix maps requirements to test cases, ensuring complete test coverage.

| Requirement ID | Requirement | Test Case ID | Test Case Title | Status |
| :--- | :--- | :--- | :--- | :--- |
| REQ-001 | User can log in with valid credentials | TC-001 | Valid User Login | ✓ Pass |
| REQ-001 | User can log in with valid credentials | TC-002 | Invalid Email Login | ✓ Pass |
| REQ-002 | User can search for products | TC-010 | Search Existing Product | ✓ Pass |
| REQ-003 | User can add items to cart | TC-020 | Add Product to Cart | ✓ Pass |

---

##  Requirements Document

The requirements document outlines the features and acceptance criteria for the application.

### Sample Requirement

```markdown
## REQ-001: User Authentication

**Description:** Users must be able to log in to the system with valid credentials.

**Acceptance Criteria:**
- User can enter email and password
- System validates credentials against database
- User is redirected to dashboard on successful login
- Error message is displayed on failed login
- Session is created and persists across page navigation
- User can log out and session is destroyed

**Priority:** Critical
**Status:** In Progress
```

---

##  Key Learnings

This repository demonstrates:
1. **Test Case Design:** Writing clear, comprehensive test cases
2. **Bug Documentation:** Professional bug reporting with all necessary details
3. **Requirements Analysis:** Understanding and documenting requirements
4. **Traceability:** Mapping requirements to test cases for complete coverage
5. **Professional Communication:** Documenting issues in a way developers understand

---

##  Related Repositories

- [qa-portfolio-overview](https://github.com/Ayoub-DataScientist/qa-portfolio-overview) - Portfolio map and overview
- [web-ui-testing-playwright](https://github.com/Ayoub-DataScientist/web-ui-testing-playwright) - Automated UI testing
- [api-testing-automation](https://github.com/Ayoub-DataScientist/api-testing-automation) - Automated API testing
- [test-automation-framework](https://github.com/Ayoub-DataScientist/test-automation-framework) - Advanced framework

---

##  License

This project is open source and available under the MIT License.
