# PG Management System

## 1. Introduction
The **PG Management System** is a full-stack web application designed to automate and manage Paying Guest accommodations. It replaces manual operations like rent tracking, tenant management, and complaint handling with a centralized digital system.

## 2. Problem Statement
Most PG owners rely on notebooks or Excel sheets. This leads to errors, lack of transparency, and inefficient tracking of tenants and payments.

## 3. Objectives
Build a scalable system using **ASP.NET Core**, **React**, and **MongoDB** that supports role-based access, automation, and analytics.

## 4. Tech Stack Explanation
- **Backend:** ASP.NET Core Web API (handles business logic)
- **Frontend:** React (UI/UX)
- **Database:** MongoDB Atlas (cloud NoSQL database)
- **Authentication:** JWT-based secure login system

## 5. System Architecture
`Client (React) → API Layer (ASP.NET Core) → Database (MongoDB)`

All communication happens via REST APIs using JSON.

## 6. User Roles
- **Admin:** Manages rooms, tenants, payments, and complaints.
- **Tenant:** Views rent, makes payments, and raises complaints.

## 7. Functional Requirements
- Authentication
- Room Management
- Tenant Management
- Payment Tracking
- Complaint System
- Dashboard Analytics

## 8. Non-Functional Requirements
- Scalability
- Security
- Performance
- Availability
- Maintainability

## 9. Database Design
### Collections
- **Users:** `Id`, `Name`, `Email`, `Role`
- **Rooms:** `RoomNumber`, `Capacity`, `Rent`, `Occupancy`
- **Tenants:** `Name`, `RoomId`, `JoinDate`
- **Payments:** `TenantId`, `Month`, `Amount`, `Status`
- **Complaints:** `TenantId`, `Description`, `Status`

## 10. API Design
- **Auth APIs:** Login/Register
- **Room APIs:** CRUD operations
- **Tenant APIs:** CRUD operations
- **Payment APIs:** Track rent
- **Complaint APIs:** Manage issues

## 11. Frontend Pages
- Landing Page
- Login/Register
- Dashboard
- Room Management
- Tenant Management
- Payment Tracking
- Complaint System

## 12. Authentication Flow
User logs in → Server validates credentials → JWT token issued → Token used for authorized API access.

## 13. Folder Structure
- **Backend:** `Controllers`, `Services`, `Repositories`, `Models`
- **Frontend:** `Components`, `Pages`, `Services`, `Hooks`

## 14. Deployment
- **Frontend:** Vercel
- **Backend:** Render or Azure
- **Database:** MongoDB Atlas

## 15. Scalability
Use indexing, caching, stateless APIs, and modular architecture to scale to thousands of users.

## 16. Maintenance
Monitor logs, update features, optimize queries, and maintain backups.

## 17. Future Enhancements
- Online payments (Razorpay)
- Notifications
- Analytics dashboard
- Mobile app
