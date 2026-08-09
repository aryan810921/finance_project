# Finance Project

A full-stack personal finance tracker built with React, Vite, Express, and MongoDB. This repository contains a modern frontend UI for tracking salary, expenses, and savings goals, along with a backend API for authentication and finance management.

## 🚀 Project Overview

This finance application helps users:
- Create a secure account
- Track salary and expenses
- Set and manage financial goals
- Review goal progress and savings insights

The repository is organized as a monorepo with separate `frontend` and `backend` applications.

## 🧱 Tech Stack

- Frontend: React, Vite, Tailwind CSS
- Backend: Express, Node.js, MongoDB, Mongoose
- Authentication: bcrypt password hashing + session tokens
- API: REST endpoints for auth and finance data

## 📁 Repository Structure

- `backend/` — Express API and MongoDB models
- `frontend/` — React application and UI components

## ⚙️ Getting Started

### 1. Backend setup

```bash
cd backend
npm install
```

Start the backend server:

```bash
npm start
```

The backend runs on `http://localhost:5000` by default.

### 2. Frontend setup

```bash
cd frontend
npm install
npm run dev
```

Open the local Vite URL shown in the terminal, typically `http://localhost:5173`.

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/register` — register a new user
- `POST /api/auth/login` — authenticate and create a session
- `POST /api/auth/logout` — invalidate the current session

### Finance
> These routes require an authorized session token in the `Authorization: Bearer <token>` header.

- `POST /api/finance` — create finance data for a user
- `PATCH /api/finance` — update salary and expense values
- `POST /api/finance/goals` — add a new finance goal
- `GET /api/finance/dashboard` — retrieve dashboard data and goal progress

## 🧠 Features

- User registration and login
- Session-based auth with tokens
- Salary, expense, and savings goal tracking
- Goal progress calculation and recommendations
- Responsive dashboard experience

## 📝 Notes

- Backend defaults to `mongodb://127.0.0.1:27017/finance-project` if `MONGO_URI` is not set.
- Frontend API base URL should be provided via `VITE_API_BASE_URL` in the frontend environment if connecting to a deployed backend.

## 💡 Development Tips

- Run backend and frontend concurrently in separate terminals
- Ensure `FRONTEND_URL` matches the address used by the frontend dev server for CORS
- Use local storage for session token persistence in the frontend app

## 📌 License

This repository is provided as-is for development and demonstration purposes.
