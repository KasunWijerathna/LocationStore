# Location & Device Management Application

A web-based application for managing locations and devices built with Next.js and Nest.js.

## Features

- User authentication with JWT
- Location management (CRUD operations)
- Device management (CRUD operations)
- Responsive design with Tailwind CSS
- MongoDB integration

## Prerequisites

- Node.js (v14 or higher)
- MongoDB Atlas account
- npm or yarn package manager

## Project Structure

```
.
├── backend/             # Nest.js backend
│   ├── src/
│   │   ├── auth/       # Authentication module
│   │   ├── users/      # Users module
│   │   ├── locations/  # Locations module
│   │   └── devices/    # Devices module
│   └── package.json
│
└── frontend/           # Next.js frontend
    ├── src/
    │   ├── app/       # Pages and routes
    │   └── contexts/  # Context providers
    └── package.json
```

## Setup & Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd location-device-management
```

2. Install backend dependencies:
```bash
cd backend
npm install
```

3. Install frontend dependencies:
```bash
cd ../frontend
npm install
```

4. Create a `.env` file in the backend directory with your MongoDB connection string:
```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

## Running the Application

1. Start the backend server:
```bash
cd backend
npm run start:dev
```

2. Start the frontend development server:
```bash
cd frontend
npm run dev
```

3. Access the application:
- Frontend: http://localhost:3001
- Backend API: http://localhost:3000

## API Endpoints

### Authentication
- POST /auth/register - Register a new user
- POST /auth/login - Login user

### Locations
- GET /locations - Get all locations
- POST /locations - Create a new location
- GET /locations/:id - Get location by ID
- PATCH /locations/:id - Update location
- DELETE /locations/:id - Delete location

### Devices
- GET /devices - Get all devices
- POST /devices - Create a new device
- GET /devices/:id - Get device by ID
- PATCH /devices/:id - Update device
- DELETE /devices/:id - Delete device

## Environment Variables

### Backend
- `MONGODB_URI` - MongoDB connection string
- `JWT_SECRET` - Secret key for JWT token generation

### Frontend
- `NEXT_PUBLIC_API_URL` - Backend API URL (default: http://localhost:3000)

## Built With

- [Next.js](https://nextjs.org/) - Frontend framework
- [Nest.js](https://nestjs.com/) - Backend framework
- [MongoDB](https://www.mongodb.com/) - Database
- [Tailwind CSS](https://tailwindcss.com/) - CSS framework
- [TypeScript](https://www.typescriptlang.org/) - Programming language 