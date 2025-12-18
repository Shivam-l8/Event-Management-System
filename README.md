# Event Management System

A full-stack application for managing events, built with React, Express, and MongoDB. Create, update, delete, and view events with a simple and intuitive user interface.

## Features

- ✨ Create, read, update, and delete events
- 📅 View event details with date, time, and location
- 📋 List all events in an organized view
- 🎨 Modern and intuitive UI built with React
- 🚀 RESTful API with Express.js

## Tech Stack

- **Frontend**: React.js, React Router, Axios, Framer Motion, Vite
- **Backend**: Express.js, Node.js
- **Database**: MongoDB with Mongoose ODM

## Project Structure

```
Event-Management-System-main/
├── backend/           # Express.js API server
│   ├── models/       # MongoDB models (Event schema)
│   ├── routes/       # API routes
│   └── index.js      # Server entry point
├── frontend/         # React.js application
│   ├── src/
│   │   ├── components/   # React components
│   │   └── services/     # API service functions
│   └── vite.config.js
└── README.md
```

## Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- MongoDB (running locally or MongoDB Atlas connection string)

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd Event-Management-System-main
```

### 2. Backend Setup

```bash
cd backend
npm install

# Create .env file from .env.example
cp .env.example .env

# Edit .env file with your MongoDB connection string
# MONGODB_URI=mongodb://localhost:27017/eventmanagement
# or
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/eventmanagement

# Start the backend server
npm run dev
```

The backend server will run on `http://localhost:5000` (or the port specified in `.env`).

### 3. Frontend Setup

```bash
cd frontend
npm install

# Create .env file from .env.example
cp .env.example .env

# Edit .env file with your API URL
# VITE_API_URL=http://localhost:5000/api/events

# Start the frontend development server
npm run dev
```

The frontend will be available at `http://localhost:5173` (default Vite port).

## Environment Variables

### Backend (.env)

- `MONGODB_URI` - MongoDB connection string (required)
  - Local: `mongodb://localhost:27017/eventmanagement`
  - Atlas: `mongodb+srv://username:password@cluster.mongodb.net/eventmanagement`
- `PORT` - Server port (optional, defaults to 5000)

### Frontend (.env)

- `VITE_API_URL` - Backend API URL (required)
  - Development: `http://localhost:5000/api/events`
  - Production: `https://your-api-domain.com/api/events`

## Available Scripts

### Backend
- `npm start` - Start production server
- `npm run dev` - Start development server with nodemon

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## API Endpoints

Base URL: `http://localhost:5000/api/events`

- `GET /api/events` - Get all events (sorted by date)
- `GET /api/events/:id` - Get a specific event by ID
- `POST /api/events` - Create a new event
- `PUT /api/events/:id` - Update an event
- `DELETE /api/events/:id` - Delete an event

### Event Schema

```javascript
{
  title: String (required),
  description: String (required),
  date: Date (required),
  time: String (required),
  location: String (required),
  organizer: String (required),
  createdAt: Date (auto-generated)
}
```

## Usage

1. Start both backend and frontend servers
2. Open the application in your browser (usually `http://localhost:5173`)
3. Create events using the event form
4. View all events in the event list
5. Click on an event to view details
6. Edit or delete events as needed

## License

ISC
