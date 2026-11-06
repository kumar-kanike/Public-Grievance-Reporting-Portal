# Public Grievance Reporting Portal

React + Node.js/Express + MongoDB application for citizens to report civic issues, track complaint status and add follow-up comments.

## Features
- Email/password authentication with bcrypt and JWT.
- Submit grievances with category, location and description.
- Private complaint history and comment threads.
- MongoDB Atlas persistence with user-scoped records.
- Responsive React dashboard.

## Stack
React, Vite, Node.js, Express, MongoDB Atlas, Mongoose.

## Database
`grievance_portal_db` — collections: `users`, `grievances`, `comments`, `departments`.

## Run
Create an Atlas database user and allow the backend host IP. Copy `backend/.env.example` to `backend/.env`, set `MONGODB_URI` and a random 32+ character `JWT_SECRET`. Then run `cd backend && npm install && npm run dev` and, in another terminal, `cd frontend && npm install && npm run dev`. Open port 5173.

## Production gap
This MVP needs authorized department accounts, moderation, status-change audit logs, anti-spam controls and a verified escalation process before it can represent official government complaint handling.
