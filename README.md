# 🛠️ GearGuard

GearGuard is a web-based Maintenance Management System designed to help organizations manage equipment, maintenance requests, maintenance teams, technicians, and preventive maintenance through a centralized dashboard.

---

# Project Overview

GearGuard is a full-stack maintenance management application built using Flask, SQLAlchemy, SQLite/PostgreSQL, and JavaScript.

The system helps organizations:

- Track company assets and equipment
- Manage maintenance requests
- Assign technicians and maintenance teams
- Schedule preventive maintenance
- Monitor maintenance history
- Generate reports and analytics
- View real-time dashboards

---

# Features

## Dashboard

- Real-time statistics
- Equipment status overview
- Maintenance request summary
- Interactive charts
- Recent activity

### Equipment Management

- Asset registration
- Equipment categories
- Equipment code generation
- Warranty tracking
- Equipment status management
- Maintenance history

### Maintenance Requests

- Corrective maintenance
- Preventive maintenance
- Priority management
- Kanban workflow
- Auto-filled request details
- Overdue detection

### Team Management

- Maintenance teams
- Team members
- Team workload tracking

### Technician Management

- Technician profiles
- Skill tracking
- Availability management

### Reports

- Equipment reports
- Maintenance reports
- Team performance
- Historical records

### Authentication

- Admin
- Manager
- Technician
- User

---

# Technology Stack

| Category | Technology |
|----------|------------|
| Backend | Flask |
| Database | SQLite / PostgreSQL |
| ORM | SQLAlchemy |
| Frontend | HTML, CSS, JavaScript |
| Charts | Chart.js |
| Calendar | FullCalendar |
| UI Framework | Bootstrap 5 |

---

# Architecture

```
Frontend (HTML, CSS, JavaScript)
            │
            ▼
      Flask Backend
            │
 ┌──────────┼──────────┐
 │ REST API │ Business │
 │          │  Logic   │
 └──────────┼──────────┘
            │
            ▼
      SQLAlchemy ORM
            │
            ▼
 SQLite / PostgreSQL
```

---

# Project Structure

```
GearGuard/

├── app.py
├── requirements.txt
├── backend/
│   ├── models/
│   ├── routes/
│   └── config.py
│
├── frontend/
│   ├── static/
│   │   ├── css/
│   │   └── js/
│   └── templates/
│
├── tests/
│
└── README.md
```

---

# Installation

Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/GearGuard.git
```

Move into the project folder

```bash
cd GearGuard
```

Create virtual environment

```bash
python -m venv venv
```

Activate environment

Windows

```bash
venv\Scripts\activate
```

Linux / Mac

```bash
source venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the application

```bash
python app.py
```

Open

```
http://localhost:5000
```

---

# API Reference

## Authentication

```
POST /auth/register
POST /auth/login
POST /auth/logout
```

## Equipment

```
GET /api/equipment
POST /api/equipment
PUT /api/equipment/{id}
DELETE /api/equipment/{id}
```

## Maintenance Requests

```
GET /api/requests
POST /api/requests
PUT /api/requests/{id}
DELETE /api/requests/{id}
```

## Teams

```
GET /api/teams
POST /api/teams
PUT /api/teams/{id}
```

## Reports

```
GET /api/reports/summary
GET /api/reports/team-performance
GET /api/reports/equipment-breakdown
```

---

# Workflow

### Corrective Maintenance

```
Equipment Failure
      ↓
Create Request
      ↓
Assign Team
      ↓
Assign Technician
      ↓
Repair Equipment
      ↓
Close Request
```

### Preventive Maintenance

```
Schedule Maintenance
      ↓
Assign Team
      ↓
Perform Maintenance
      ↓
Update Status
      ↓
Maintenance History
```

---

# Testing

Start the application

```bash
python app.py
```

Run API tests

```bash
python test_api_like_user.py
```

Run comprehensive backend tests

```bash
python comprehensive_backend_test.py
```

---

# Database Schema

Main Entities

- User
- Role
- Equipment
- Equipment Category
- Maintenance Request
- Maintenance Team
- Technician
- Maintenance Stage

Relationship

```
User
 │
 └── Role

Equipment
 │
 ├── Category
 ├── Team
 └── Maintenance Request

Maintenance Request
 │
 ├── Technician
 └── Stage
```

---

# Smart Features

- Equipment auto-fill
- Automatic team assignment
- Preventive maintenance scheduling
- Warranty tracking
- Kanban workflow
- Dashboard analytics
- Maintenance history
- Calendar integration
- Role-based access control
- Overdue request detection

---

# Future Improvements

- Email notifications
- QR code support
- Mobile application
- Predictive maintenance
- IoT integration
- Export reports to PDF and Excel
- Advanced analytics dashboard
