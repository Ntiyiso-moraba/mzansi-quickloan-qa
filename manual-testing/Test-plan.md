# Test Plan: MzansiQuickLoan Origination Portal

**Prepared By:** Ntiyiso Moraba (QA Tester)  
**Date:** 12 November 2026  
**Project Version:** v1.0 (Phase 1 – Manual Functional Testing)  

---

## 1. Overview
As part of the MzansiQuickLoan quality assurance initiative, this Test Plan outlines the high-level testing strategy, scope, tools, environment, design techniques, and schedule required to validate the MzansiQuickLoan Personal Loan Origination Portal before release.

## 2. Scope

### 2.1 In Scope
* **Input Field Validations:** Full Name, 13-digit South African ID Number (numeric & minimum age 18+), Net Monthly Income, Existing Monthly Debt, Credit Score (300–850), Loan Amount (R1,000–R50,000), and Repayment Term (6, 12, 24 months).
* **Business Logic & Calculations:** Credit score threshold check (minimum 600), 30% net disposable income affordability rule, and 15% per annum interest calculation.
* **UI & User Feedback:** Field placeholders, "Assess Loan Application" button functionality, and dynamic status alerts (Approved, Declined, Validation Error).

### 2.2 Out of Scope
* Backend database persistence and user account authentication.
* Live credit bureau API integrations and automated email/SMS notifications.
* Mobile native application testing (Phase 1 covers desktop web only).

## 3. Tools & Technologies Used
* **Test Case Management & Traceability:** Google Sheets & Microsoft Excel (`.xlsx`)
* **Defect & Issue Tracking:** Linear (Board View, Severity/Priority Triage)
* **Version Control & Repository Hosting:** Git & GitHub (Feature Branching & Pull Requests)
* **Local Hosting & Inspection:** VS Code Live Server & Chrome DevTools

## 4. Test Environment
* **Operating System:** Windows 10 / 11
* **Browsers:** Google Chrome (Latest), Microsoft Edge (Latest)
* **Local Server:** VS Code Live Server (`http://127.0.0.1:5500`)

## 5. Test Strategy & Approach
* **Test Design Techniques:** Boundary Value Analysis (BVA), Equivalence Partitioning, Error Guessing, and Exploratory Testing.
* **Testing Types:**
  * *Smoke Testing:* Verify core page load and primary submission flow before deep testing.
  * *Functional & UI Testing:* Validate every input field and business rule against the Software Requirements Specification (SRS).
  * *Usability Testing:* Ensure error and approval messages are clear, accurate, and user-friendly.
  * *Regression Testing:* Re-execute test cases after defect fixes are applied.
* **Best Practices:** Context-Driven Testing, Shift-Left QA principles, and End-to-End user flow validation.

## 6. Defect & Test Tracking Procedures
* **Test Documentation:** Test Scenarios and Test Cases maintained in Excel/CSV and Markdown inside GitHub (`manual-testing/`).
* **Defect Tracking:** All functional and UI defects logged in **Linear** with Severity, Priority, Steps to Reproduce, Expected vs. Actual Results, and screenshots.
* **Reporting:** Daily QA progress summary tracking executed test cases, pass/fail rates, and open blockers.

## 7. Roles & Responsibilities
* **Ntiyiso Moraba (QA Tester):** Test plan creation, test scenario/case design, manual test execution, exploratory testing, defect logging in Linear, and GitHub documentation.

## 8. Test Schedule

| Task / Milestone | Duration | Target Date |
| :--- | :--- | :--- |
| Requirement Analysis & Test Plan Creation | 1 Day | 12 Nov 2026 |
| Test Scenario & Test Case Design (12 Cases) | 1 Day | 13 Nov 2026 |
| Test Execution, Bug Hunting & Linear Logging | 1 Day | 15 Nov 2026 |
| GitHub Portfolio Push & LinkedIn Showcase | 1 Day | 15 Nov 2026 |

