# 👔 HR Management System - Project Planning Document

## 📋 Project Overview

Custom HR management system for tracking employee attendance, overtime, leaves, coaching, payroll, and performance across agents, teams, sites, and accounts.

---

## 🎯 STEP 1: Requirements & Features

### **Feature Categories:**

#### 1️⃣ **AUTHENTICATION & EMPLOYEE ACCOUNTS**

- Employee login system
- Each agent has personal account
- Role-based access (Agent, Team Leader, Manager, HR, Admin)
- Avatar upload
- Change name & password
- View personal salary & deductions

#### 2️⃣ **ATTENDANCE & TIME TRACKING**

- Auto login tracking at shift start time
- Auto logout tracking at shift end
- Late arrival detection & auto deduction
- Break time tracking
- Manual attendance override (for HR/Manager)
- Attendance history view

#### 3️⃣ **OVERTIME TRACKER**

- Track overtime hours per agent
- Automatic calculation from login/logout times
- Overtime approval workflow
- View overtime history
- Calculate overtime pay

#### 4️⃣ **LEAVES MANAGEMENT**

- Leave request submission
- Leave types: sick, annual, emergency
- Approval workflow (Team Lead → Manager)
- Leave balance tracking
- Leave history & calendar view
- Deduction for unpaid leaves

#### 5️⃣ **COACHING SYSTEM**

- Track failed attributes at:
  - Agent level
  - Team level
  - Site level
  - Account level
- Coaching sessions tracking
- Agent acknowledgment of coaching
- Warning letter generation & tracking
- Coaching count per agent
- Performance improvement plans

#### 6️⃣ **PAYROLL & SALARY MANAGEMENT**

- View salary breakdown (base + overtime + bonuses)
- Real-time salary tracking (increases/decreases)
- Auto deductions:
  - Late arrivals
  - Absences
  - Unpaid leaves
  - Penalties
- Manual deductions (by HR)
- Salary history & trends
- Payslip generation

#### 7️⃣ **DEDUCTIONS SYSTEM**

- Auto deduction for late login
- Absence deductions
- Warning-based deductions
- Manual deduction entry
- Deduction history per agent
- Deduction rules configuration

#### 8️⃣ **COMMISSIONS & BONUSES**

- Commission tracking per agent
- Bonus allocation
- Performance-based incentives
- Commission calculation rules

#### 9️⃣ **SHIFT MANAGEMENT**

- Multiple shift types (morning, evening, night)
- Shift schedules per agent
- Shift swap requests
- Off days tracking

#### 🔟 **RECRUITING MODULE**

- Job postings
- Candidate tracking
- Interview scheduling
- Offer letters
- Onboarding checklist

#### 1️⃣1️⃣ **REPORTING & ANALYTICS**

- Agent performance dashboard
- Team performance comparison
- Site-level statistics
- Account-level metrics
- Attendance reports
- Payroll reports
- Export to Excel/PDF

#### 1️⃣2️⃣ **SETTINGS**

- Salary rules configuration
- Deduction rules
- Shift timings
- Leave policies
- Late arrival threshold
- Overtime rates

---

## 📑 STEP 2: Pages Structure

### **Main Pages:**

1. **Login Page** (`/login`)

   - Employee authentication

2. **Dashboard** (`/dashboard`)

   - Personal overview for agents
   - Team/Site overview for managers
   - Quick stats & alerts

3. **My Profile** (`/profile`)

   - View/edit personal info
   - Avatar upload
   - Change password

4. **My Salary** (`/salary`)

   - Current month salary
   - Salary breakdown
   - Salary history & trends
   - Download payslips

5. **My Attendance** (`/attendance`)

   - Login/logout button (auto-tracked)
   - Today's attendance status
   - Attendance history
   - Late arrivals count

6. **My Leaves** (`/leaves`)

   - Leave balance
   - Submit leave request
   - Leave history & status

7. **My Overtime** (`/overtime`)

   - Overtime hours this month
   - Overtime history
   - Submit overtime request

8. **Coaching (Agent View)** (`/coaching`)

   - My coaching sessions
   - Failed attributes
   - Acknowledge coaching
   - View warning letters

9. **Employees Management** (`/employees`) - _HR/Manager only_

   - All employees list
   - Add/edit/deactivate employees
   - Assign shifts & teams

10. **Attendance Management** (`/attendance/manage`) - _HR/Manager_

    - View all attendance
    - Manual corrections
    - Attendance reports

11. **Coaching Management** (`/coaching/manage`) - _Manager/QA_

    - Create coaching session
    - Assign to agent
    - Track acknowledgments
    - Issue warning letters
    - View coaching statistics

12. **Payroll Management** (`/payroll`) - _HR only_

    - Process monthly payroll
    - Review deductions
    - Manual adjustments
    - Generate payslips

13. **Reports** (`/reports`)

    - Attendance reports
    - Performance reports
    - Payroll reports
    - Custom reports

14. **Recruiting** (`/recruiting`) - _HR only_

    - Job postings
    - Candidates pipeline
    - Interview schedules

15. **Settings** (`/settings`) - _Admin only_
    - System configuration
    - Salary rules
    - Deduction rules
    - Shift timings

---

## 🔧 STEP 3: Feature Categories Breakdown

### **Category A: Core Authentication & Employee Profiles**

**Features:**

- Login/Logout
- Role-based access control
- Employee accounts with personal data
- Avatar upload
- Password management
- Employee CRUD (HR)

---

### **Category B: Attendance & Auto Tracking** ⏰

**Features:**

- Auto login/logout tracking
- Late detection with configurable threshold
- Auto deduction calculation
- Break time tracking
- Manual attendance corrections
- Attendance history & reports

---

### **Category C: Overtime & Leaves**

**Features:**

- Overtime tracking & approval
- Overtime pay calculation
- Leave request workflow
- Leave balance management
- Leave calendar
- Integration with attendance

---

### **Category D: Coaching System** 📋

**Features:**

- Failed attributes tracking (agent/team/site/account)
- Coaching session creation
- Agent acknowledgment workflow
- Warning letter generation
- Coaching count tracking
- Performance analytics

---

### **Category E: Payroll & Salary System** 💰 (Most Complex)

**Features:**

- Salary calculation engine
- Real-time salary tracking
- Auto deductions (late, absence, penalties)
- Manual deductions
- Commission & bonus tracking
- Salary history & trends
- Payslip generation
- Salary breakdown view

---

### **Category F: Shift Management & Off Days**

**Features:**

- Shift scheduling
- Multiple shift types
- Shift swap requests
- Off days tracking
- Shift roster view

---

### **Category G: Recruiting Module** (Optional)

**Features:**

- Job postings
- Candidate pipeline
- Interview scheduling
- Offer management
- Onboarding checklist

---

### **Category H: Reports & Analytics** 📊

**Features:**

- Performance dashboards
- Attendance reports
- Payroll reports
- Team/Site/Account analytics
- Export functionality (Excel/PDF)
- Custom report builder

---

### **Category I: Settings & Configuration**

**Features:**

- Salary rules management
- Deduction rules
- Shift configuration
- Leave policies
- Late threshold settings
- Overtime rates

---

---

## 📅 STEP 4: 5-Phase Development Plan

### **Phase 1: Foundation & Employee Management** (2.5 weeks)

**Deliverables:**

- Project setup (React + Node.js + PostgreSQL)
- Database schema design
- Authentication with roles (Agent, Manager, HR, Admin)
- Employee management (CRUD)
- Profile management with avatar
- Basic dashboard layout

**Completion Criteria:**
✅ Employees can login with role-based access  
✅ HR can create/manage employee accounts  
✅ Employees can view/edit their profiles

---

### **Phase 2: Attendance & Auto Tracking** (2.5 weeks)

**Deliverables:**

- Auto login/logout tracking system
- Late arrival detection
- Auto deduction calculation
- Break time tracking
- Attendance history view
- Manual attendance corrections (HR)
- Integration with shift schedules

**Completion Criteria:**
✅ System auto-tracks login/logout times  
✅ Late arrivals trigger auto deductions  
✅ Employees see their attendance history  
✅ HR can make manual corrections

---

### **Phase 3: Payroll, Overtime & Leaves** (3 weeks)

**Deliverables:**

- Salary calculation engine
- Real-time salary tracking (view increases/decreases)
- Auto deductions integration
- Manual deductions (HR)
- Overtime tracking & approval
- Leave request workflow
- Leave balance management
- Payslip generation

**Completion Criteria:**
✅ Employees see real-time salary breakdown  
✅ Auto deductions calculated correctly  
✅ Overtime & leaves tracked and approved  
✅ Payslips generated monthly

---

### **Phase 4: Coaching System & Shift Management** (2.5 weeks)

**Deliverables:**

- Failed attributes tracking (agent/team/site/account levels)
- Coaching session creation & tracking
- Agent acknowledgment system
- Warning letter generation
- Coaching count tracking
- Shift scheduling & management
- Off days tracking
- Shift swap requests

**Completion Criteria:**
✅ Managers can create coaching sessions  
✅ Agents acknowledge coaching  
✅ Warning letters generated and tracked  
✅ Shifts assigned and tracked

---

### **Phase 5: Reports, Settings & Deployment** (2 weeks)

**Deliverables:**

- Performance dashboards (agent/team/site/account)
- Attendance reports
- Payroll reports
- Export to Excel/PDF
- Settings page (salary rules, deduction rules, etc.)
- Final UI polish
- Bug fixes
- Testing
- Deployment
- Documentation

**Completion Criteria:**
✅ All reports working and exportable  
✅ Settings configurable by admin  
✅ System tested and deployed  
✅ Documentation complete

---

## 🛠 STEP 5: Technology Decisions

### **Frontend:**

- **Framework:** React 18 with TypeScript
- **Routing:** React Router v6
- **State Management:** React Query + Zustand
- **Styling:** Tailwind CSS
- **Forms:** React Hook Form + Zod validation
- **Charts:** Recharts or Chart.js
- **Date Handling:** date-fns
- **Tables:** TanStack Table (React Table)
- **UI Components:** shadcn/ui or custom components

### **Backend:**

- **Runtime:** Node.js 20+
- **Framework:** Express.js
- **Database:** PostgreSQL 15
- **ORM:** Prisma
- **Authentication:** JWT + bcrypt
- **File Upload:** Multer (for avatars & documents)
- **Validation:** Zod
- **Scheduling:** Node-cron (for auto tracking & deductions)
- **PDF Generation:** PDFKit or Puppeteer (for payslips)

### **DevOps & Hosting:**

- **Frontend:** Vercel or Netlify
- **Backend:** Railway, Render, or DigitalOcean
- **Database:** Supabase, Neon, or Railway PostgreSQL
- **File Storage:** Cloudinary or AWS S3
- **Version Control:** Git + GitHub
- **CI/CD:** GitHub Actions

### **Additional Tools:**

- **Real-time:** Socket.io (for live notifications)
- **Email:** Nodemailer or SendGrid (for notifications)
- **Excel Export:** ExcelJS
- **PDF Export:** PDFKit

---

## 📝 Technical Challenges & Solutions

### **Challenge 1: Auto Login/Logout Tracking**

**Solution:**

- Use Node-cron to run scheduled tasks
- Check if employee has logged in at shift start time
- If not, mark as "late" and calculate deduction
- Store timezone-aware timestamps
- Allow manual override by HR

### **Challenge 2: Real-time Salary Calculation**

**Solution:**

- Create salary calculation engine
- Recalculate on every event:
  - Late arrival → deduct
  - Leave approved → deduct (if unpaid)
  - Overtime approved → add
  - Manual adjustment → update
- Cache calculations for performance
- Show breakdown: base + additions - deductions

### **Challenge 3: Multi-level Coaching Tracking**

**Solution:**

- Database structure:
  - Agent → Team → Site → Account hierarchy
  - Failed attributes table with level column
  - Aggregation queries for statistics
- Use PostgreSQL views for reporting
- Index properly for performance

---

## 🎯 Success Metrics

### **Phase 1 Success:**

- [ ] 100 employees can login
- [ ] HR can create employee accounts
- [ ] Employees see personal dashboard

### **Phase 2 Success:**

- [ ] System tracks login/logout automatically
- [ ] Late arrivals trigger deductions
- [ ] 95%+ accuracy in time tracking

### **Phase 3 Success:**

- [ ] Employees see correct salary breakdown
- [ ] Deductions calculated automatically
- [ ] Payslips generated accurately

### **Phase 4 Success:**

- [ ] Coaching sessions tracked
- [ ] Warning letters generated
- [ ] Shifts assigned correctly

### **Phase 5 Success:**

- [ ] All reports accurate
- [ ] System handles 100 employees smoothly
- [ ] Zero critical bugs

---

**Document Created:** December 2025  
**Project Type:** HR Management System  
**Target Users:** 100+ employees across multiple teams/sites  
**Target Platform:** Web Application (Desktop primary, Mobile responsive)
