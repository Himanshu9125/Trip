# Trip Booking Application

This project is a full-stack ride-booking application inspired by Uber. It allows users to book rides, captains to accept rides, and provides real-time ride tracking using Google Maps.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)

---

## Features

### User Features:
- User registration and login.
- Book rides by entering pickup and destination locations.
- View fare estimates for different vehicle types.
- Real-time ride tracking using Google Maps.
- Logout functionality.

### Captain Features:
- Captain registration and login.
- Accept or reject ride requests.
- Update location in real-time.
- Start and complete rides.

### General Features:
- Secure authentication using JWT.
- Socket.io for real-time communication between users and captains.
- Google Maps integration for location suggestions, distance calculation, and live tracking.

---

## Technologies Used

### Frontend:
- **React**: For building the user interface.
- **Vite**: For fast development and build tooling.
- **Tailwind CSS**: For styling.
- **Socket.io-client**: For real-time communication.
- **Google Maps API**: For location services.

### Backend:
- **Node.js**: For server-side logic.
- **Express.js**: For building RESTful APIs.
- **MongoDB**: For database storage.
- **Socket.io**: For real-time communication.
- **Google Maps API**: For geocoding and distance calculations.

---

## Project Structure
Trip/ ├── Backend/ │ ├── controllers/ │ ├── db/ │ ├── middlewares/ │ ├── models/ │ ├── routes/ │ ├── services/ │ ├── app.js │ ├── server.js │ └── socket.js ├── frontend/ │ ├── public/ │ ├── src/ │ │ ├── components/ │ │ ├── context/ │ │ ├── pages/ │ │ ├── App.jsx │ │ ├── main.jsx │ │ └── index.css │ ├── package.json │ ├── vite.config.js │ └── tailwind.config.js └── .gitignore

## Setup Instructions

### Prerequisites:
- Node.js and npm installed.
- MongoDB installed and running locally or on a cloud service.
- Google Maps API key.

### Backend Setup:
1. Navigate to the `Backend` directory:
   ```bash
   cd Backend
2. Install dependencies:
npm install
3. Create a .env file in the Backend directory and configure the following variables:
DB_CONNECT=<your_mongodb_connection_string>
_jJWT_SECRET=<yourwt_secret>
MAPS_API=<your_google_maps_api_key>
4. Start the backend server
   node [server.js](http://localhost:4000)
**Frontend Setup:**
1. Navigate to the frontend directory:
   cd frontend
2. Install dependencies:
   npm install
3. Create a .env file in the frontend directory and configure the following variables:
   VITE_BASE_URL=http://localhost:3000
   VITE_GOOGLE_MAPS_API_KEY=<your_google_maps_api_key>
5. Start the frontend development server:
   npm run dev
**Environment Variables:**
Backend:
 DB_CONNECT: MongoDB connection string.
 JWT_SECRET: Secret key for JWT authentication.
 GOOGLE_MAPS_API: Google Maps API key.
Frontend:
 VITE_BASE_URL: Base URL for the backend API.
 VITE_GOOGLE_MAPS_API_KEY: Google Maps API key.
API Endpoints
User Endpoints:
 POST /users/register: Register a new user.
 POST /users/login: Login a user.
 GET /users/profile: Get user profile.
 GET /users/logout: Logout a user.
Captain Endpoints:
 POST /captains/register: Register a new captain.
 POST /captains/login: Login a captain.
 GET /captains/profile: Get captain profile.
 GET /captains/logout: Logout a captain.
Ride Endpoints:
 POST /rides/create: Create a new ride.
 GET /rides/get-fare: Get fare estimate.
 POST /rides/confirm: Confirm a ride.
 GET /rides/start-ride: Start a ride.
 POST /rides/end-ride: End a ride.
Maps Endpoints:
 GET /maps/get-coordinates: Get coordinates for an address.
 GET /maps/get-distance-time: Get distance and time between two locations.
 GET /maps/get-suggestions: Get location suggestions.
