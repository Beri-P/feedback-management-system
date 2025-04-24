# Customer Feedback Management System

A platform where businesses can create custom surveys, distribute them via various channels, and analyze the results.

## Table of Contents

1. [Features](#features)  
2. [Tech Stack](#tech-stack)  
3. [Getting Started](#getting-started)  
   1. [Prerequisites](#prerequisites)  
   2. [Installation](#installation)  
   3. [Environment Variables](#environment-variables)  
   4. [Running the App](#running-the-app)  
4. [Testing](#testing)  
5. [Deployment](#deployment)  
6. [Contributing](#contributing)  
7. [License](#license)

---

## Features

- **Survey builder** with multiple question types (text, rating, multiple-choice)  
- **Distribution** via email or shareable link  
- **Response collection** with real-time storage in Supabase  
- **Analytics dashboard** (charts, filters, exports)  
- **Authentication & role management** (admin, editor, viewer)  
- **Mobile-responsive** UI

## Tech Stack

- **Backend:** Node.js & Express, Supabase (PostgreSQL + Auth), Jest & Supertest  
- **Frontend:** React, TypeScript, Vite, Tailwind CSS, ShadCN UI, Redux Toolkit  
- **DevOps:** Docker (local), Vercel/Render (production)

---

## Getting Started

### Prerequisites

- **Node.js** v14+ (we recommend v20 LTS)  
- **npm** or **yarn**  
- **Git**

### Installation

1. **Clone the repo**  
   ```bash
   git clone https://github.com/<your-username>/feedback-management-system.git
   cd feedback-management-system

2.  **Backend setup**

```bash
cd backend
npm install
cp .env.example .env
# 👉 Edit `backend/.env` with your Supabase URL & service-role key:
#    SUPABASE_URL=https://xyzabc.supabase.co
#    SUPABASE_KEY=your_service_role_key_here
```

3. **Frontend setup**

```bash
cd frontend
npm install
# (optional) scaffold Tailwind & shadcn if you haven’t yet:
# npx tailwindcss init -p
# npx shadcn@latest init --legacy-peer-deps
npm run dev
```

4. **Environment Variables**
Copy and fill in .env.example in backend/:

PORT=5000
NODE_ENV=development
JWT_SECRET=your_jwt_secret_here
SUPABASE_URL=https://xyzabc.supabase.co
SUPABASE_KEY=your_service_role_key_here

5. **Running the App**
If you didn’t start them above:

```bash
# Backend (port 5000)
cd backend
npm run dev

# Frontend (port 5173)
cd ../frontend
npm run dev
```

6. **Testing**

```bash
# Backend tests
cd backend
npm test

# Frontend tests (if any)
cd frontend
npm test
```

7. **Deployment**

**Backend**: Docker image → Vercel/Render with your .env vars

**Frontend**: Vite production build → Vercel/Netlify


8. **Contributing**

Fork the repo

Create a feature branch

Commit your changes

Push and open a Pull Request