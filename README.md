# 🏆 Rewards & Recognition Application

A Flutter desktop application for managing employee rewards and recognition with automated evaluation, multi-level approval workflow, and comprehensive reporting.

---

## ✨ Features

- **Smart Evaluation System**: 6-criteria scoring (100 points) with automatic reward tier recommendation
- **Multi-Level Approval**: 3-tier approval workflow with department-based routing
- **Employee Management**: Bulk Excel import or manual entry
- **Award Rules**: Configurable category rules displayed during submission
- **Duplicate Prevention**: Max 2 rewards/year per employee, no duplicate categories
- **Advanced Reports**: Excel export with date/department filters
- **Real-time Dashboard**: Statistics, pending approvals, and trends

---

## 🛠️ Tech Stack

- **Flutter 3.x** (Desktop - Windows/macOS/Linux)
- **SQLite** (sqflite_common_ffi)
- **Excel** package for import/export
- **Material Design 3** UI

---

## 📦 Installation

```bash
# Clone repository
git clone https://github.com/yourusername/rewards-recognition-app.git
cd rewards-recognition-app

# Install dependencies
flutter pub get

# Run application
flutter run -d windows

# Build for production
flutter build windows --release
```

**Default Login:** `admin` / `admin123` ⚠️ Change after first login!

---

## 📊 Evaluation System

**6 Criteria (100 Points Total):**
1. Savings Potential (45 pts) - Annual cost savings
2. Intangible Benefit (25 pts) - Non-monetary impact
3. Feasibility (10 pts) - Implementation ease
4. Investment Required (10 pts) - % of savings
5. Creativity (5 pts) - Innovation level
6. Implementation Type (5 pts) - Organizational scope

**Reward Tiers:**
- 🥇 Platinum (91-100): ₹1,00,000
- 🥇 Gold (81-90): ₹75,000
- 🥈 Silver (71-80): ₹50,000
- 🎖️ Certificate + Voucher (61-70): ₹25,000
- 📜 Certificate (0-60): ₹10,000

---

## 👥 User Roles

- **Admin**: Full access, manage users/employees/categories
- **Nominator**: Submit rewards with evaluation
- **Approver Level 1/2/3**: Department/tier-based approvals

---

## 🗄️ Database Schema

**4 Main Tables:**
- `users` - Authentication & roles
- `employees` - Employee master data
- `reward_categories` - Award types with rules
- `rewards` - Nominations with evaluation scores

---

## 📖 Quick Start Guide

### Submit Reward
1. Login → "Submit Reward"
2. Select employee (autocomplete)
3. Fill 6 evaluation criteria
4. System calculates score & suggests tier
5. Review award rules & monetary value
6. Submit for approval

### Approve Rewards
1. Dashboard → "Pending Approvals"
2. Review evaluation & reason
3. Approve/Reject with comments
4. Auto-routes to next level

### Excel Import (Employees)
**Required columns:** Employee ID, Full Name, Department  
**Optional:** Position, Email, Manager ID

---

## 🔒 Security Notes

⚠️ **Before Production:**
- Implement password hashing (currently plain text)
- Configure secure database path
- Enable audit logging
- Set session timeouts

---

## 📁 Project Structure

```
lib/
├── main.dart
├── models/models.dart
├── database/databasehelper.dart
└── pages/
    ├── login_page.dart
    ├── dashboard_page.dart
    ├── submit_reward_page.dart
    ├── approval_page.dart
    ├── manage_categories_page.dart
    ├── employee_management_page.dart
    ├── user_management_page.dart
    └── reports_page.dart
```



