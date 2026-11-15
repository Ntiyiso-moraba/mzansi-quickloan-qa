# MzansiQuickLoan — End-to-End QA Portfolio Project

A functional quality assurance project validating a South African micro-loan origination web application against real-world credit, affordability, and identity compliance rules.

## Project Scope & Business Rules Tested
* **Identity & Age Validation:** 13-digit numeric South African ID verification and minimum applicant age (18+ via `YYMMDD`).
* **Loan Limits:** Boundary validation for R1,000 minimum and R50,000 maximum loan amounts.
* **Affordability Assessment:** Monthly installment capped at 30% of net disposable income (`Net Income - Existing Monthly Debt`).
* **Credit Score Threshold:** Minimum required score of `600`.
* **Interest Calculation:** 15% per annum simple interest across 6, 12, and 24-month terms.

## QA Artifacts & Deliverables
* **[Test Plan](manual-testing/Test-plan.md):** Scope, test design techniques (BVA, Equivalence Partitioning, Error Guessing), environment, and schedule.
* **[Test Scenarios & Test Cases](manual-testing/MzansiQuickLoan_Test_Cases.xlsx):** 5 traced test scenarios and 12 executed test cases with exact test data and pass/fail results.
* **[Defect Tracking (Linear)](manual-testing/screenshot/linear-bug-board.png):** 5 functional and boundary defects logged with reproduction steps, expected vs. actual results, and severity/priority triage.

## Key Defects Uncovered
1. **Non-numeric SA ID accepted (`TC_001`):** Input accepts 13 alphabetic letters instead of enforcing digits only.
2. **Under-18 applicant approved (`TC_001`):** Missing age verification on the `YYMMDD` birth date prefix.
3. **Existing monthly debt ignored (`TC_008`):** Affordability check calculates 30% of gross income without subtracting existing debt obligations.
4. **Boundary credit score failure (`TC_009`):** Off-by-one bug (`<= 600`) declines eligible applicants with a score of exactly `600`.
5. **24-month interest miscalculation (`TC_012`):** Applies 15% flat interest instead of 15% per annum (`30%` total over 2 years).

## Tools Used
* **Test Management & Defect Tracking:** Linear, Google Sheets / Excel
* **Version Control & Agile Workflow:** Git, GitHub
* **Application Under Test:** HTML5, CSS3, JavaScript (`app/index.html`)

