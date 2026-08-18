# Library Management System (LMS) — Requirements

*Derived from the Trello board `Library Management System` (Sprint 1 - To Do: US-01–US-05; Backlog/Sprint 2: US-06–US-10).*

---

## 1. Functional Requirements (FR)

### FR-01 — Search Catalog *(US-01, High, Sprint 1)*
- FR-01.1: The system shall allow a member to search the catalog by **title**, **author**, or **ISBN**.
- FR-01.2: The system shall return matching results for any valid title, author, or ISBN.
- FR-01.3: The system shall display a "no results found" message for an empty or no-match query.
- FR-01.4: Search shall be **case-insensitive** and support **partial matches**.

### FR-02 — Borrow Book *(US-02, High, Sprint 1)*
- FR-02.1: The system shall allow a member to borrow an available book.
- FR-02.2: The system shall only permit borrowing if a copy is available **and** the member has no unpaid fines.
- FR-02.3: The system shall automatically set the loan due date to **14 days** from the issue date.
- FR-02.4: The system shall update the copy status to **"On Loan"** immediately upon borrowing.

### FR-03 — Return Book *(US-03, High, Sprint 1)*
- FR-03.1: The system shall allow a member to return a borrowed book.
- FR-03.2: The system shall update the copy status to **"Available"** upon return.
- FR-03.3: The system shall automatically calculate a fine if the return is overdue.
- FR-03.4: The system shall send the member a confirmation of successful return.

### FR-04 — View Borrowing History *(US-04, Medium, Sprint 1)*
- FR-04.1: The system shall display all past and current loans, including issue, due, and return dates.
- FR-04.2: The system shall visually flag overdue loans.
- FR-04.3: The system shall sort the loan list with the most recent loan first.

### FR-05 — Manage Catalog *(US-05, High, Sprint 1)*
- FR-05.1: The system shall allow a librarian to add a new book with title, author, ISBN, and category.
- FR-05.2: The system shall allow a librarian to edit or remove an existing catalog entry.
- FR-05.3: The system shall reflect catalog changes immediately in member search results.

### FR-06 — Reserve Book *(US-06, Medium, Sprint 2)*
- FR-06.1: The system shall allow a member to reserve a book only when **no copies are currently available**.
- FR-06.2: The system shall notify the member when a reserved copy becomes available.
- FR-06.3: The system shall automatically expire a reservation if not claimed within **48 hours** of notification.

### FR-07 — Manage Member Accounts *(US-07, Medium, Sprint 2)*
- FR-07.1: The system shall allow a librarian to register a new member account.
- FR-07.2: The system shall allow a librarian to suspend or reactivate an existing member account.
- FR-07.3: The system shall prevent suspended members from borrowing or reserving books.

### FR-08 — Generate Overdue Reports *(US-08, Medium, Sprint 2)*
- FR-08.1: The system shall allow a librarian to generate a report listing all loans past their due date.
- FR-08.2: The report shall include member contact information and days overdue.
- FR-08.3: The system shall allow the report to be exported/downloaded.

### FR-09 — Pay Fines Online *(US-09, Low, Sprint 2)*
- FR-09.1: The system shall allow a member to view their total fines owed.
- FR-09.2: The system shall allow a member to pay a partial or full fine amount online.
- FR-09.3: The system shall update the account's fine balance immediately after payment.

### FR-10 — Admin Usage Reports *(US-10, Low, Sprint 2)*
- FR-10.1: The system shall allow an admin to view usage reports showing active loans, members, and books borrowed per period.
- FR-10.2: The report data shall be accurate as of the current date.
- FR-10.3: The system shall allow the report to be filtered by date range.

---

## 2. Non-Functional Requirements (NFR)

| ID | Category | Requirement | Source |
|----|----------|-------------|--------|
| NFR-01 | Performance | Catalog search results shall load within **2 seconds** of query submission. | US-01 |
| NFR-02 | Reliability | Loan due dates shall be calculated consistently and automatically (14 days from issue) with no manual intervention. | US-02 |
| NFR-03 | Data Integrity | Copy status ("On Loan" / "Available") shall update immediately and accurately on borrow/return actions. | US-02, US-03 |
| NFR-04 | Reliability | Overdue fines shall be calculated automatically and accurately at the point of return. | US-03 |
| NFR-05 | Usability | Borrowing history shall be clearly presented, with overdue items visually distinguishable at a glance. | US-04 |
| NFR-06 | Consistency | Catalog edits made by librarians shall propagate to member-facing search **immediately** (no noticeable sync delay). | US-05 |
| NFR-07 | Availability | The reservation-notification and 48-hour expiry mechanism shall run reliably without missed or late expirations. | US-06 |
| NFR-08 | Security / Access Control | Account suspension shall take effect immediately, blocking borrow/reserve actions system-wide for that member. | US-07 |
| NFR-09 | Security | Role-based access control shall restrict catalog management, member management, and reporting to authorized librarian/admin roles. | US-05, US-07, US-08, US-10 |
| NFR-10 | Data Integrity / Compliance | Fine payments shall update account balances immediately and accurately; payment handling shall follow secure payment-processing standards. | US-09 |
| NFR-11 | Maintainability | Reports (overdue, usage) shall be exportable/downloadable in a maintainable format for follow-up and analysis. | US-08, US-10 |
| NFR-12 | Scalability | The system shall support concurrent search, borrow, return, and reservation actions from multiple members without performance degradation. | Cross-cutting |
| NFR-13 | Notification Delivery | Return confirmations and reservation-availability alerts shall be delivered promptly to members. | US-03, US-06 |

---

## 3. Traceability Summary

| Story ID | Title | Priority | List / Sprint | Points | Due Date | Assignee |
|----------|-------|----------|----------------|--------|----------|----------|
| US-01 | Search Catalog | 🔴 High | Sprint 1 | 3 | 08/15/2026 | Member A |
| US-02 | Borrow Book | 🔴 High | Sprint 1 | 5 | 08/19/2026 | Member A |
| US-03 | Return Book | 🔴 High | Sprint 1 | 3 | 08/20/2026 | Member B |
| US-04 | View Borrowing History | 🟡 Medium | Sprint 1 | 3 | 08/22/2026 | Member B |
| US-05 | Manage Catalog | 🔴 High | Sprint 1 | 5 | 08/25/2026 | Member C |
| US-06 | Reserve Book | 🟡 Medium | Backlog (Sprint 2) | 5 | 08/31/2026 | Member A |
| US-07 | Manage Member Accounts | 🟡 Medium | Backlog (Sprint 2) | 5 | 09/01/2026 | Member C |
| US-08 | Generate Overdue Reports | 🟡 Medium | Backlog (Sprint 2) | 5 | 09/04/2026 | Member C |
| US-09 | Pay Fines Online | 🟢 Low | Backlog (Sprint 2) | 3 | 09/06/2026 | Member B |
| US-10 | Admin Usage Reports | 🟢 Low | Backlog (Sprint 2) | 8 | 09/09/2026 | Member A |

**Sprint 1 total points:** 19 &nbsp;|&nbsp; **Sprint 2 (Backlog) total points:** 26 &nbsp;|&nbsp; **Total:** 45
