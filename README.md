# DriveMate: Smart Travel & Vehicle Assistance Management System

DriveMate is a comprehensive, production-ready full-stack mobile application designed to streamline the car rental experience. It integrates vehicle management, trip planning, real-time tracking, and emergency assistance into a single unified platform.

## 🚀 Core Features & Integrated Modules

The system is built around 6 interconnected modules that follow a logical story-based data flow:

1.  **Fleet Management & Admin Control**: Admins manage the vehicle inventory, setting critical parameters like price per day, fuel efficiency (km/L), and tank capacity.
2.  **Booking & Smart Payments**: Users can browse cars, select rental dates, and upload bank transfer receipts. The system calculates base prices and generates professional PDF invoices upon admin approval.
3.  **Destination Exploration**: A curated list of tourist destinations in Sri Lanka. Users can explore spots and add them directly to their upcoming trip plans.
4.  **Interactive Trip Planner & Timetable**: Users can schedule their itineraries day-by-day.
    *   **Map Logic**: The system uses a **Simulated Google Maps Distance Matrix API** logic. It mathematically calculates travel durations and distances between consecutive stops to provide a realistic schedule without incurring external API costs during the development phase.
    *   **Ticket Management**: Users can upload photos of entrance tickets or safari passes directly to each stop.
    *   **Smart Reminders**: Simulated push notification logic alerts users about upcoming scheduled stops.
5.  **Intelligent Fuel Tracking**: Integrates with the Booking module to fetch the car's fuel efficiency. It calculates real-time range (km remaining) and tank percentage based on user logs.
6.  **Emergency SOS & Incident Reporting**:
    *   **Emergency Dial**: Uses the **Native Linking API** to instantly trigger the device's dialer to call emergency services (119) with a single tap.
    *   **GPS Integration**: Uses the **Expo Location API** to capture precise GPS coordinates during accidents or breakdowns.
    *   **Damage Reporting**: Users can upload real-time photos of damages. The admin side provides a full-screen image viewer for detailed inspection and can generate formal PDF Accident Reports.

---

## 🛠 Tech Stack

### Backend (Node.js & Express)
- **Express.js**: RESTful API architecture.
- **MongoDB & Mongoose**: Scalable NoSQL database with strict schema validation.
- **JWT & Bcrypt**: Secure token-based authentication and password hashing.
- **Multer**: Sophisticated multipart file handling with dynamic directory nesting.
- **PDFKit**: Automated server-side generation of Invoices and Reports.

### Frontend (React Native & Expo)
- **React Native (Expo)**: Cross-platform mobile development.
- **Context API**: Global state management for authentication and user preferences.
- **React Navigation**: Seamless stack and tab-based navigation.
- **Reanimated & Lucide**: Smooth micro-animations and modern iconography.
- **Axios**: Robust HTTP client for backend communication.

---

## 📁 Project Structure

### Root Directory
- `backend/`: Node.js server and API logic.
- `frontend/`: React Native mobile application.
- `README.md`: Project documentation.

### Backend Structure
- `server.js`: Application entry point and route mounting.
- `controllers/`: Core business logic for each of the 6 modules.
- `models/`: MongoDB schemas (User, Car, Booking, TripPlan, SOS, etc.).
- `routes/`: API endpoint definitions.
- `middleware/`: Authentication and file upload processors.
- `uploads/`: Organized storage for car images, receipts, and PDF exports.

### Frontend Structure
- `App.js`: Root component with navigation providers.
- `src/screens/`: Feature-specific screens (Booking, Trip, Admin, etc.).
- `src/components/`: Reusable UI elements (Modals, Custom Buttons, Reviews).
- `src/context/`: Authentication and Global State providers.
- `src/theme/`: Centralized design system (Colors, Shadows, Typography).

---

## 🔧 Installation & Setup

1.  **Backend**:
    ```bash
    cd backend
    npm install
    npm run dev
    ```
2.  **Frontend**:
    ```bash
    cd frontend
    npm install
    npx expo start

## ⚖️ System Logic & Math
The system relies on several custom algorithms:
- **Price Calculation**: `(PricePerDay * Days) + AddOns`.
- **Fuel Math**: `(CurrentFuel / TankCapacity) * 100` for percentage; `CurrentFuel * kmPerLiter` for range.
- **Penalty Logic**: Automated 10% penalty calculation for cancellations of approved bookings.

## My Contribution

As a member of the development team, I was primarily responsible for the Vehicle Management and Admin Control Module.

**Responsibilities**
Developed vehicle management functionalities including:
       Add Vehicle
       Update Vehicle Details
       Delete Vehicle
       View Vehicle Information
       Implemented CRUD operations for vehicle records.
       Developed administrative interfaces for fleet management.
       Integrated vehicle-related database operations using MongoDB.
       Implemented validation and data handling for vehicle management processes.
       Participated in testing, debugging, and integration of the module with the overall system.

## Key Learning Outcomes
  Full-Stack Mobile Application Development
  REST API Development
  MongoDB Database Design
  CRUD Operations Implementation
  React Native Application Development
  Software Engineering Best Practices
  Team-Based Project Development
  Version Control with Git and GitHub
  
## Academic Project
This project was developed as part of 2 year 2 semester Web development and Mobile Application module learning activity at Sri Lanka Institute of Information Technology (SLIIT).

## Application Screenshots

### Home Screen

<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/0c6f9f96-0d8e-4c24-befd-85cf6b29d5ae" />

### Booking System

<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/806211e1-9ebe-439a-bec9-26936dc11e3d" />
<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/4683088c-39b0-4e8c-8f40-69055baa1c48" />
<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/059ed7c4-bc53-4a0e-9f58-2b001aa66e70" />
<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/47b7516a-1655-41ad-bd47-bb4da91ee585" />
<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/617fac71-519e-4ee7-b832-cfc78ca5a401" />
<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/af327508-6993-454f-b921-7f0abf149708" />

### Fuel Management

<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/3ec53b5c-abd5-4f4e-84a2-c9c921fe1034" />

### SOS & Emergency

<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/0c26d218-9a31-444c-a97f-6dbf360bc4d5" />
<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/3f2c9f5e-cb41-409e-b986-73709ab64558" />
<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/8b7f7ae2-1d61-41da-bc78-93a8f2dc32a7" />

### Review Management

<img width="520" height="1000" alt="image" src="https://github.com/user-attachments/assets/ac861928-4ae4-420a-9d1c-f1f2a9b03f0f" />

### Vehicle managemt and admin Dashboard




