# Comprehensive HR Management System (HRMS) - Call Center Edition

## 1. Project Overview
[cite_start]A highly dynamic HR management system tailored for call center operations, covering the full employee lifecycle from recruitment and training to performance auditing and payroll[cite: 1, 4].

---

## 2. Organization Structure & Hierarchy (New)
The system supports a dynamic organization chart to manage departments and reporting lines:
* [cite_start]**Department Management:** Ability to create new departments/accounts and assign a Manager to each[cite: 78].
* **Reporting Lines:** * Every **Agent/Trainee** must be linked to a specific **Team Leader**.
    * Every **Team Leader** must be linked to a **Manager/Supervisor**.
* **Visual Org Chart:** A tree-view interface to visualize the chain of command within the company.

---

## 3. User Roles (7 Roles)
| Role | Responsibility | Key Permissions |
| :--- | :--- | :--- |
| **CEO / Admin** | System Governance | [cite_start]Full access, system-level configurations, and audit logs[cite: 12, 152]. |
| **GM** | Operations Oversight | [cite_start]View-only access to all analytics and site-level comparisons[cite: 77, 95]. |
| **HR** | Personnel Admin | [cite_start]Full lifecycle management, payroll, and recruitment control[cite: 124, 138, 148]. |
| **Quality (QA)** | Quality Auditing | [cite_start]Evaluates calls, tracks failed attributes, and initiates PIPs[cite: 33, 42]. |
| **Team Leader** | Team Management | [cite_start]Performance tracking, shift approvals, and coaching[cite: 12, 132]. |
| **Agent** | Employee | [cite_start]Personal dashboard, attendance, and real-time salary view[cite: 11, 14, 94]. |
| **Training Agent**| Probationary Hire | Access to training materials and progress tracking (1-6 months). |

---

## 4. Training & Probation Module (Updated)
* **Duration:** Flexible duration (1 to 6 months) based on account needs.
* **Outcome Workflows:**
    * **Passed:** HR promotes the user to "Agent" status; they receive 100% of their salary.
    * **Failed:** The user is terminated and receives 50% of the final month's salary.
* [cite_start]**Management:** HR has the authority to change status and manage the graduation checklist[cite: 73].

---

## 5. Performance & Dynamic KPI System

* **Evaluation Sources:**
    * [cite_start]**Team Leader:** Focuses on general performance, productivity, and behavior[cite: 132].
    * [cite_start]**Quality (QA):** Focuses on call quality metrics and specific failed attributes[cite: 33, 121].
* [cite_start]**Dynamic KPIs:** Admin/HR can define KPI types (AHT, Quality, CSAT) with custom weights and targets per agent or account[cite: 60, 61, 82].
* [cite_start]**Warning Letters:** Automated system for Verbal, Written (1 & 2), and Final warnings with mandatory agent acknowledgment[cite: 40, 123].

---

## 6. Recruitment & Application Module
* **Public Application Form:** An external-facing form where candidates submit personal data and CVs.
* [cite_start]**Candidate Pipeline:** Auto-reflects submissions into the HR recruitment dashboard[cite: 70, 150].
* [cite_start]**Filtering & CV Analysis:** Tools for HR to filter candidates, rate experience, and move them through interview stages[cite: 71, 151].
* **Blacklist:** A "Blacklist" section for rejected candidates to prevent future applications for specific reasons.

---

## 7. Dynamic Configuration (No Hardcoding)
* [cite_start]**Deduction Engine:** HR/Admin can configure late arrival tiers and grace periods via UI[cite: 56, 84, 87].
* [cite_start]**Batch Controls:** Apply specific deduction or OT rules to a selection of agents or accounts[cite: 56].
* [cite_start]**Overtime Rates:** Configurable rates (1.5x, 2.0x, etc.) based on day type[cite: 24, 88].
* [cite_start]**Shift Management:** Define shift windows (Morning, Mid, Night) and shift differential pay[cite: 64, 85].

---

## 8. Announcements Module
* [cite_start]**Creation:** Exclusive to **Admin** and **HR**[cite: 152, 148].
* **Reach:** Visible to all roles (Training Agent through GM).
* [cite_start]**Categories:** Internal job postings, policy changes, events, and urgent alerts[cite: 69].
* **Engagement:** Track views and required digital acknowledgment for policy updates.

---

## 9. Payroll & Real-Time Salary
* [cite_start]**Live Calculation:** `Base Salary + OT + Bonuses - (Dynamic Deductions + Absences) = Net Salary`[cite: 44, 49].
* [cite_start]**Real-time Preview:** Agents can see their current month's salary updating daily based on attendance and performance[cite: 44, 102].
* [cite_start]**HR Override:** HR has full control to manually adjust, add, or remove deductions before final processing[cite: 49, 141].

---

## 10. Technical Requirements
* [cite_start]**Real-time Updates:** Use WebSockets for attendance status and notification alerts[cite: 16, 95].
* [cite_start]**Security:** Role-Based Access Control (RBAC) and data encryption for financial records[cite: 12].
* [cite_start]**Exporting:** All reports (Payroll, Attendance, QA) must be exportable to PDF/Excel[cite: 81].
