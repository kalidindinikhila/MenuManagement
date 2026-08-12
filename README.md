# Menu Management System

A full-stack restaurant menu management system that enables restaurant owners to efficiently manage menus, categories, orders, billing, QR menus, and staff through an intuitive web application.

## Architecture

The application follows a modern client-server architecture with a React frontend, NestJS backend, PostgreSQL database, and Prisma ORM for efficient database management.

# Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React + Vite + Tailwind CSS |
| Backend | NestJS |
| Database | PostgreSQL |
| ORM | Prisma |
| Authentication | JWT |
| API Testing | Postman |

---

# Features

### Authentication
- Secure JWT-based Login
- Restaurant Registration
- Role-Based Access Control
- Staff PIN Switching

### Menu Management
- Create Menu Categories
- Add, Update, Delete Menu Items
- Item Variations
- Add-ons Management
- Price Management

### Table Management
- Floor Plan Management
- Table Status Tracking
- Table Availability

### Order Management
- Create Orders
- Add/Remove Items
- Kitchen Order Ticket (KOT)
- Order Status Tracking

### Billing
- GST Calculation
- Discount Support
- Split Payments
- Invoice Generation
- Bill History

### Reports
- Daily Sales Report
- Payment Summary
- Item-wise Sales
- Revenue Analytics

### QR Menu
- QR Code Generation
- Digital Menu Viewing
- Contactless Menu Access

---

# Prerequisites

Before running the project, install:

- Node.js (18+)
- PostgreSQL
- Git
- Visual Studio Code

Verify installation:

```powershell
node -v
npm -v
git --version
psql --version
```

---

# Installation

Clone the repository:

```powershell
git clone https://github.com/kalidindinikhila/MenuManagement.git

cd MenuManagement
```

---

# Database Setup

Create a PostgreSQL database:

```sql
CREATE DATABASE menumanagement;
```

Create a user:

```sql
CREATE USER menuadmin WITH PASSWORD 'password';
GRANT ALL PRIVILEGES ON DATABASE menumanagement TO menuadmin;
```

---

# Backend Setup

```powershell
cd backend
npm install
copy .env.example .env
```

Configure `.env`

```env
DATABASE_URL="postgresql://menuadmin:password@localhost:5432/menumanagement"

JWT_SECRET=your_secret_key
```

Push the database schema:

```powershell
npx prisma db push
```

Seed the database:

```powershell
npm run db:seed
```

Run backend:

```powershell
npm run start:dev
```

Backend URL

```
http://localhost:3000/api
```

---

# Frontend Setup

Open another terminal:

```powershell
cd frontend
npm install
npm run dev
```

Frontend URL

```
http://localhost:5173
```

---

# Demo Login

Email

```
admin@demo.com
```

Password

```
password123
```

---

# Project Structure

```
MenuManagement/
│
├── backend/
│   ├── prisma/
│   ├── src/
│   │   ├── auth/
│   │   ├── billing/
│   │   ├── menus/
│   │   ├── orders/
│   │   ├── reports/
│   │   ├── tables/
│   │   └── users/
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── assets/
│   └── package.json
│
├── docs/
├── docker-compose.yml
└── README.md
```

---

# Workflow

1. Login to the application.
2. Register a restaurant (first-time setup).
3. Create menu categories.
4. Add menu items.
5. Manage restaurant tables.
6. Create customer orders.
7. Send Kitchen Order Tickets (KOT).
8. Generate bills.
9. Track sales and reports.

---

# API Modules

- Authentication
- Users
- Menu
- Orders
- Billing
- Reports
- QR Menu
- Table Management

---

# Production

Backend

```powershell
npm run build
npm run start:prod
```

Frontend

```powershell
npm run build
```

Production files are generated inside:

```
frontend/dist
```

---

# Future Enhancements

- Online Ordering
- Customer Mobile Application
- Kitchen Display System (KDS)
- Inventory Management
- AI-based Sales Analytics
- Loyalty & Rewards Program

---
