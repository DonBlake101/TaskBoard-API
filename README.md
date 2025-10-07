# Expense Tracker API

A clean **Node.js + Express** REST API to log expenses with **JWT auth**, **Jest/Supertest** tests, and **GitHub Actions** CI.  
Uses an in-memory store to keep setup simple (swap to a DB later).

## Features
- Auth: `POST /auth/login` returns a demo JWT (no DB)
- CRUD: list/create/delete expenses (protected routes)
- Tests: Jest + Supertest
- CI: GitHub Actions workflow runs tests on every push/PR

## Tech Stack
Express • JSON Web Tokens • Jest • Supertest • GitHub Actions

## Endpoints
- `GET /` → health check  
- `POST /auth/login` → `{ token }`
- `GET /expenses` (auth) → `[{ id, title, amount, category, date }]`
- `POST /expenses` (auth) → `{ title, amount:number, category?, date? }`
- `DELETE /expenses/:id` (auth)

## Quickstart
```bash
npm install
cp .env.example .env
npm test
npm run dev
# http://localhost:3000

