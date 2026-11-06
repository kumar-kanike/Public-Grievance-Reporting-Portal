# Public Grievance Reporting Portal

A React + Node.js + MongoDB application for citizens to report civic issues, track complaint status, and add follow-up comments.

## Features
- Email/password registration and login (bcrypt + JWT).
- Submit grievances with category, location and description.
- Private complaint history and comment thread per complaint.
- MongoDB Atlas persistence and user-scoped queries.
- Responsive React dashboard.

## Stack
React, Vite, Node.js, Express, MongoDB Atlas, Mongoose, JWT, bcrypt.

## Database
- Database: `grievance_portal_db`
- Collections: `users`, `grievances`, `comments`, `departments`

## Run locally
1. Create an Atlas database user and allow the backend host IP in Network Access.
2. Copy `backend/.env.example` to `backend/.env`; set the MongoDB connection string and a random JWT secret of at least 32 characters.
3. Start the API: `cd backend && npm install && npm run dev`.
4. In another terminal start the UI: `cd frontend && npm install && npm run dev`.
5. Open port 5173. Vite proxies `/api` to the backend on port 5000.

## Important
This is an MVP. A real civic deployment needs authorized department accounts, moderation, status-change audit logs, anti-spam controls, privacy/retention rules, and a verified escalation process. Do not represent demo submissions as officially filed government complaints.
