# Student Authentication & Profile Management

## Prerequisites
- Node.js >= 14
- npm
- MongoDB (local or Atlas)

## Setup Backend
1. `cd backend`
2. Copy `.env.example` -> `.env` and fill values (MONGO_URI, JWT_SECRET)
3. `npm install`
4. `mkdir uploads` (for profile photos)
5. `npm run dev` (uses nodemon) or `node server.js`

## Setup Frontend
1. `cd frontend`
2. `npm install`
3. `npm start`

Frontend runs on http://localhost:3000 (default). Backend default port is 5000.

## API Endpoints
- `POST /api/auth/register` — register user (multipart/form-data for photo)
- `POST /api/auth/login` — login (json { email, password })
- `GET /api/auth/me` — get current user (requires `Authorization: Bearer <token>`)
- `PUT /api/auth/me` — update profile (multipart/form-data allowed)
