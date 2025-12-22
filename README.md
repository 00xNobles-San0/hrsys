# AmenDBS Call Center ERP

## 1. Project Overview
A highly dynamic HR management system tailored for call center operations, covering the full employee lifecycle from recruitment and training to performance auditing and payroll.

---

## 2. Organization Structure & Hierarchy
The system supports a dynamic organization chart to manage departments and reporting lines.

### Features
- **Department Management:** Create departments/accounts and assign a Manager to each.
- **Reporting Lines:**
  - Every **Agent / Training Agent** must be linked to a **Team Leader**.
  - Every **Team Leader** must be linked to a **Manager / Supervisor**.
- **Visual Org Chart:** Tree-view interface to visualize the chain of command.

---

## 3. User Roles (7 Roles)

| Role | Responsibility | Key Permissions |
|-----|---------------|----------------|
| **CEO / Admin** | System Governance | Full access, system-level configuration, audit logs |
| **GM** | Operations Oversight | View-only access to analytics and site comparisons |
| **HR** | Personnel Administration | Employee lifecycle, payroll, recruitment |
| **Quality (QA)** | Quality Auditing | Call evaluations, failed attributes, PIPs |
| **Team Leader** | Team Management | Performance tracking, shift approvals, coaching |
| **Agent** | Employee | Dashboard, attendance, real-time salary |
| **Training Agent** | Probationary Hire | Training access and progress tracking (1–6 months) |

---

## 4. Training & Probation Module

- **Duration:** Flexible (1 to 6 months).
- **Outcome Workflows:**
  - **Passed:** Promoted to Agent with 100% salary.
  - **Failed:** Terminated with 50% of final month salary.
- **Management:** HR controls status changes and graduation checklist.

---

## 5. Performance & Dynamic KPI System

### Evaluation Sources
- **Team Leader:** Productivity, behavior, general performance.
- **Quality (QA):** Call quality metrics and failed attributes.

### Key Features
- **Dynamic KPIs:** Admin/HR can define KPIs (AHT, Quality, CSAT) with custom weights and targets per agent or account.
- **Warning Letters:** Automated verbal, written (1 & 2), and final warnings with mandatory agent acknowledgment.

---

## 6. Recruitment & Application Module

- **Public Application Form:** External form for candidate data and CV uploads.
- **Candidate Pipeline:** Applications automatically appear in HR dashboard.
- **Filtering & CV Analysis:** Candidate filtering, experience rating, and interview stage management.
- **Blacklist:** Prevents reapplication for rejected candidates based on defined reasons.

---

## 7. Dynamic Configuration (No Hardcoding)

- **Deduction Engine:** Configure late tiers and grace periods via UI.
- **Batch Controls:** Apply deduction or OT rules to selected agents or accounts.
- **Overtime Rates:** Configurable (1.5x, 2.0x, etc.) by day type.
- **Shift Management:** Define shift windows (Morning, Mid, Night) and differential pay.

---

## 8. Announcements Module

- **Creation:** Admin and HR only.
- **Visibility:** Available to all roles.
- **Categories:** Job postings, policies, events, urgent alerts.
- **Engagement Tracking:** View tracking and mandatory digital acknowledgment.

---

## 9. Payroll & Real-Time Salary

- **Live Formula:**
- **Real-Time Preview:** Daily salary updates based on attendance and performance.
- **HR Override:** Manual adjustment before final payroll processing.

---

## 10. Technical Requirements

- **Real-Time Updates:** WebSockets for attendance and notifications.
- **Security:** Role-Based Access Control (RBAC) and encrypted financial data.
- **Exporting:** Payroll, Attendance, and QA reports exportable to PDF and Excel.
