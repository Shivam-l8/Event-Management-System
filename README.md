# Event Management System

A full-stack Event Management System built with **React (Vite)**, **Express.js**, and **MongoDB**. It supports creating, viewing, updating, and deleting events through a clean UI and a REST API.

> Security note: Do **not** commit real secrets (MongoDB URIs, API keys). Use `.env` locally and keep it in `.gitignore`.

## Features

- ✨ Create, read, update, and delete events
- 📅 Event details (date, time, location, organizer)
- 📋 List and view all events in an organized layout
- 🎨 Modern UI built with React + Vite
- 🚀 RESTful API with Express.js + Mongoose

## Tech Stack

- **Frontend**: React, React Router, Axios, Framer Motion, Vite
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose ODM)

## Project Structure

Event-Management-System/
├── backend/                 # Express API
│   ├── models/              # Mongoose schemas
│   ├── routes/              # API routes
│   ├── index.js             # Server entry
│   ├── package.json
│   ├── .env.example         # Example env (safe)
│   └── .gitignore
├── frontend/                # React (Vite)
│   ├── src/
│   │   ├── components/
│   │   └── services/
│   ├── vite.config.js
│   ├── package.json
│   ├── .env.example         # Example env (safe)
│   └── .gitignore
└── README.md

## Prerequisites

- Node.js v16+
- npm or yarn
- MongoDB (local) or MongoDB Atlas

## Getting Started

### 1) Clone

git clone <repository-url>
cd Event-Management-System

### 2) Backend Setup

cd backend
npm install

# Create .env from example
cp .env.example .env

# Start backend
npm run dev

Backend runs on:
- http://localhost:5000 (default) or the PORT in .env

### 3) Frontend Setup

cd ../frontend
npm install

# Create .env from example
cp .env.example .env

# Start frontend
npm run dev

Frontend runs on:
- http://localhost:5173 (default Vite port)

## Environment Variables

### Backend (backend/.env)

MONGODB_URI=your_mongodb_connection_string_here
PORT=5000

Examples:
- Local: mongodb://localhost:27017/eventmanagement
- Atlas (placeholder format): mongodb+srv://<username>:<password>@<cluster-url>/eventmanagement

### Frontend (frontend/.env)

VITE_API_URL=http://localhost:5000/api/events

## API Endpoints

Base URL (dev): http://localhost:5000/api/events

- GET /api/events — Get all events (sorted by date)
- GET /api/events/:id — Get event by ID
- POST /api/events — Create event
- PUT /api/events/:id — Update event
- DELETE /api/events/:id — Delete event

## Event Schema (Mongoose)

{
  title: String (required),
  description: String (required),
  date: Date (required),
  time: String (required),
  location: String (required),
  organizer: String (required),
  createdAt: Date (auto-generated)
}

## Usage

1. Start backend + frontend
2. Open http://localhost:5173
3. Create events using the form
4. View, edit, and delete events from the list

## License

ISC
