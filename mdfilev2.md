

Markdown

# HR Management System (HRMS) - Call Center Edition

## 1. Project Overview
A comprehensive, full-stack HR Management System specifically engineered for call center operations. This system manages the entire employee lifecycle—from recruitment and training to performance tracking and payroll—with a heavy emphasis on dynamic configuration and real-time monitoring.

## 2. Technical Stack
* **Frontend:** React.js, TypeScript, Material-UI (MUI), Redux Toolkit/Zustand.
* **Backend:** Node.js, Express.js, TypeScript.
* **Database:** PostgreSQL (Relational data), Redis (Caching/Sessions).
* **Real-time:** Socket.io (Attendance/Notifications).
* **Storage:** AWS S3 (CVs, documents, payslips).
* **Auth:** JWT with Role-Based Access Control (RBAC).

---

## 3. User Roles & Permissions
| Role | Primary Responsibility | Key Permissions |
| :--- | :--- | :--- |
| **Training Agent** | New Hires (Months 1-3) | View training materials, track personal progress. |
| **Agent** | Standard Employee | Clock in/out, view own salary/KPIs, request leaves. |
| **Team Leader** | Middle Management | Manage 10-15 agents, 1st level approvals, coaching. |
| **Quality Assurance**| Performance Audit | Call monitoring, issuing PIPs, tracking failed attributes. |
| **HR** | Personnel Admin | Full employee lifecycle, payroll processing, recruitment. |
| **GM** | Operations Oversight | View-only access to all analytics and site comparisons. |
| **CEO** | System Governance | **Full Access.** Configure salary rules, OT rates, and audit logs. |

---

## 4. System Modules

### A. Dynamic Configuration (No Hardcoding)
* **Deductions:** Tiered late arrival rules (e.g., 6-10 mins = X EGP) and grace periods.
* **Overtime:** Configurable multipliers (Regular 1.5x, Weekend 2.0x, etc.).
* **KPIs:** Custom targets (AHT, FCR, CSAT) with weighted percentages per agent.
* **Shifts:** 5 configurable shift windows with differential pay settings.

### B. Recruitment & Onboarding
* **Workflow:** Job Posting → Candidate Sourcing → CV Analysis → Interview → Offer → Onboarding.
* **Blacklist:** Permanent "do not hire" status with reason tracking.
* **CV Analysis:** Standardized HR form to evaluate experience vs. budget.

### C. Performance & Coaching
* **QA Evaluations:** Deep-dive tracking of "Failed Attributes" at Agent, Team, Site, and Account levels.
* **Disciplinary Action:** Automated workflow for Verbal, Written, and Final warnings.
* **PIP:** 30/60/90-day Performance Improvement Plans with goal tracking.

### D. Payroll & Attendance
* **Real-Time Salary:** Agents see an updating "Live Salary" based on daily attendance/OT.
* **Automated Deductions:** System auto-calculates penalties based on late clock-ins.
* **Payslips:** Automated PDF generation with full breakdown of bonuses and deductions.

---

## 5. Database Schema (Conceptual)



### Key Entities:
* `Users`: ID, Name, RoleID, ShiftID, BaseSalary, Status.
* `Attendance`: UserID, ClockIn, ClockOut, IPAddress, LateMinutes, DeductionApplied.
* `KPI_Metrics`: Type, Target, Weight, AgentID, Score.
* `Warnings`: UserID, Level (Verbal/Written/Final), IssueDate, AcknowledgedAt.
* `Recruitment`: CandidateID, Status, CV_URL, InterviewScore.

---

## 6. API Structure (High-Level)
| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/api/auth/login` | POST | Authenticate user & return JWT. |
| `/api/attendance/clock-in` | POST | Log timestamp and IP for start of shift. |
| `/api/payroll/preview/:id` | GET | Calculate real-time salary for current month. |
| `/api/admin/config/deductions`| PUT | CEO update to late-arrival penalty tiers. |
| `/api/qa/coaching` | POST | Create coaching session/warning for agent. |

---

## 7. Implementation Guidelines
1.  **Phase 1: Foundation.** Setup RBAC, Database migrations, and basic Profile management.
2.  **Phase 2: Attendance.** Implement WebSocket-based clocking and late-detection logic.
3.  **Phase 3: Performance.** QA forms, Warning Letter workflows, and KPI tracking.
4.  **Phase 4: Payroll.** Engine for calculating net salary based on dynamic rules.
5.  **Phase 5: Recruitment.** Candidate pipeline and onboarding checklist.
6.  **Phase 6: Reporting.** Dashboards for GM/CEO using Chart.js/Recharts.

---

## 8. Critical Requirements
* **Audit Trail:** Every change to salary or attendance must be logged (Who, What, When).
* **Security:** Data encryption for sensitive financial info.
* **Responsiveness:** Must be fully functional on tablets for Floor Supervisors.
* **Localization:** Support for English and Arabic UI.
