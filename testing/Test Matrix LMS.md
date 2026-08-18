# Library Management System - Test Matrix

| Test Case ID | Test Level | Related Requirement | Scenario Type | Objective | Preconditions | Status |
|---|---|---|---|---|---|---|
| LMS_UT_01 | Unit | FR-01 | Positive | Verify user login with valid credentials | System online | **Pass** |
| LMS_UT_02 | Unit | FR-01 | Negative | Reject login with incorrect password | System online | **Pass** |
| LMS_UT_03 | Unit | FR-02 | Positive | Calculate fine for overdue item ($0.25/day) | Book overdue | **Pass** |
| LMS_UT_04 | Unit | FR-02 | Negative | Reject negative values for overdue days | Book record selected | **Fail** |
| LMS_UT_05 | Unit | FR-03 | Positive | Validate ISBN-13 format input | Catalog module active | **Pass** |
| LMS_IT_01 | Integration | FR-03 | Positive | Verify catalog search queries database | Catalog & DB online | **Pass** |
| LMS_IT_02 | Integration | FR-04 | Positive | Checkout flow (Patron Service to Catalog) | Patron active, Book available | **Pass** |
| LMS_IT_03 | Integration | FR-04 | Negative | Block checkout if patron has overdue fines > $10 | Patron has $12 fine | **Fail** |
| LMS_IT_04 | Integration | FR-05 | Negative | Handle database timeout during return sync | Network delay simulated | **Fail** |
| LMS_ST_01 | System | FR-05 | Positive | Complete end-to-end book issuance workflow | System staging active | **Pass** |
| LMS_ST_02 | System | FR-06 | Positive | Complete book return with overdue fine assessment | Overdue book scanned | **Pass** |
| LMS_ST_03 | System | FR-06 | Negative | Prevent duplicate return of available book | Book is 'Available' | **Pass** |
| LMS_ST_04 | System | FR-07 | Negative | Concurrency check on simultaneous book checkout | 2 librarians active | **Pass** |
| LMS_UAT_01 | UAT | FR-08 | Positive | Patron searches catalog via OPAC kiosk | OPAC Kiosk active | **Pass** |
| LMS_UAT_02 | UAT | FR-09 | Positive | Librarian processes bulk returns | Circulation desk | **Fail** |
| LMS_UAT_03 | UAT | FR-10 | Negative | Patron attempts self-renewal past max renewals limit | Patron portal | **Pass** |
| LMS_UAT_04 | UAT | FR-11 | Negative | Unauthorized patron attempts administrative access | Patron logged in | **Pass** |

## Test Summary

| Test Level | Total | Pass | Fail | Pass Rate |
|---|---:|---:|---:|---:|
| Unit Testing | 5 | 4 | 1 | 80.0% |
| Integration Testing | 4 | 3 | 1 | 75.0% |
| System Testing | 4 | 4 | 0 | 100.0% |
| User Acceptance Testing | 4 | 3 | 1 | 75.0% |
| **Total** | **17** | **14** | **3** | **82.4%** |
