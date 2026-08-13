# 📚 Library Management System

## Project Overview

The **Library Management System (LMS)** is a software project developed to replace manual, paper-based library record-keeping with a digital system that supports searching, borrowing, returning, and reserving books, along with fine management and administrative reporting. The project was carried out using Agile practices (Sprint-based development tracked on Trello), version-controlled through Git/GitHub, modeled with UML diagrams prior to implementation, and validated through a structured testing process (unit, integration, system, and user acceptance testing).

---

## Problem Statement

Traditional library systems that rely on manual logbooks or spreadsheets face several recurring issues:

- Difficulty tracking which books are currently borrowed, overdue, or available
- No efficient way for members to search the catalog or check book availability remotely
- Manual fine calculation is error-prone and inconsistent
- No centralized way to manage reservations for high-demand books
- Librarians lack quick access to reports (overdue loans, usage trends) needed for decision-making

These inefficiencies lead to lost books, delayed returns, member dissatisfaction, and increased administrative workload. The Library Management System addresses these problems by digitizing and automating the core library workflows.

---

## Objectives

1. Design and develop a system that allows members to **search, borrow, return, and reserve** books through a digital interface.
2. Automate **fine calculation** for overdue books and allow members to view and pay fines.
3. Provide librarians with tools to **manage the catalog** (add/edit/remove books) and **manage member accounts**.
4. Enable **report generation** (e.g., overdue loans, system usage) to support library administration.
5. Apply a structured software development process — requirements gathering, UML-based design, Agile sprint planning, version control, and testing — to produce a well-documented, maintainable system.

---

## Scope

### In Scope
- Member functions: catalog search, borrowing, returning, reserving, viewing loan history, paying fines
- Librarian functions: catalog management, member account management, report generation
- Admin functions: system-wide usage reporting
- Supporting project artifacts: user stories/backlog, Sprint plan, UML diagrams (Use Case, Class, Sequence, Activity), test cases and test matrix, and version-controlled source code

### Out of Scope
- Integration with external library networks or inter-library loan systems
- Mobile native applications (web-based access only, for this phase)
- Payment gateway integration for fines (handled as a simulated/placeholder flow)
- Barcode/RFID hardware integration (assumed handled manually by library staff in this phase)

---

## Methodology

The project followed an Agile, iterative approach:

| Phase | Description |
|---|---|
| **Requirements** | Gathered and documented as user stories in a product backlog |
| **Planning** | Backlog prioritized and estimated (story points); Sprint 1 scoped to core borrowing features |
| **Design** | System modeled with UML diagrams (Use Case, Class, Sequence, Activity) before development |
| **Development** | Implemented using a Git feature-branch workflow with pull requests and code review |
| **Testing** | Verified through Unit, Integration, System, and User Acceptance Testing, tracked in a requirements-to-test matrix |
| **Review** | Repository and documentation finalized and reviewed before submission |

## Team & Responsibilities

| Member | Responsibility |
|---|---|
| **Member 1** | Project Management — backlog, Sprint planning, Trello board, Gantt chart |
| **Member 2** | System Design & GitHub — repository setup, UML diagrams, branching/PR workflow |
| **Member 3** | Testing & Repository Finalization — test cases, test matrix, repository review |

## Project Artifacts

- Product backlog & Sprint plan: [`requirements/user_stories.md`](requirements/user_stories.md)
- UML diagrams: [`/design`](design)
- Test cases & test matrix: [`testing/test_cases_library_system.xlsx`](testing/test_cases_library_system.xlsx)
- Project timeline: [`management/gantt_chart_library_system.xlsx`](management/gantt_chart_library_system.xlsx)
- File-by-file ownership: [`FILE_STRUCTURE_GUIDE.md`](FILE_STRUCTURE_GUIDE.md)
