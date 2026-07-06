# 🥗 Nutrition Assistant – Personalized Nutrition Management System

A full-stack **MERN (MongoDB, Express.js, React.js, Node.js)** web application that helps users maintain a healthy lifestyle by providing personalized nutrition guidance, meal planning, calorie tracking, BMI calculation, and diet recommendations.

---

## 📖 Overview

Nutrition Assistant is designed to assist users in managing their daily nutritional intake through an interactive and user-friendly interface. The application allows users to register, track meals, calculate BMI and calorie requirements, receive personalized nutrition recommendations, and monitor their daily dietary progress

The project follows the **Model-View-Controller (MVC)** architecture, providing a clean, modular, scalable, and maintainable codebase.

---

# 🚀 Features

### 👤 User Management

- User Registration
- User Login
- JWT Authentication
- Profile Management

### 🥗 Nutrition Management

- Meal Planner
- Daily Meal Tracking
- Nutrition Calculator
- BMI Calculator
- Calorie Requirement Calculator
- Personalized Diet Recommendations
- Daily Nutrition Log

### 📊 Dashboard

- Nutrition Summary
- Daily Calories
- Meal History
- Progress Monitoring

### 🔒 Security

- JWT Authentication
- Password Encryption (bcryptjs)
- Protected Routes
- Environment Variables

---

# 🛠 Technology Stack

## Frontend

- React.js
- Vite
- Bootstrap
- Axios
- React Router DOM
- HTML5
- CSS3
- JavaScript

## Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT Authentication
- bcryptjs
- dotenv
- CORS

---

# 🏗 Project Architecture

```
Nutrition-Assistant
│
├── client
│   ├── public
│   ├── src
│   │   ├── assets
│   │   ├── components
│   │   ├── pages
│   │   ├── services
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── package.json
│   └── vite.config.js
│
├── server
│   ├── config
│   ├── controllers
│   ├── middleware
│   ├── models
│   ├── routes
│   ├── .env
│   ├── server.js
│   └── package.json
│
├── README.md
└── .gitignore
```

---

# ⚙ Installation

## Clone Repository

```bash
git clone https://github.com/your-username/Nutrition-Assistant.git
```

Open the project folder.

```bash
cd Nutrition-Assistant
```

---

# 📦 Install Frontend Dependencies

```bash
cd client
npm install
```

---

# 📦 Install Backend Dependencies

Open another terminal.

```bash
cd server
npm install
```

---

# 🗄 Configure MongoDB

Create a **.env** file inside the **server** folder.

```env
MONGO_URI=mongodb://127.0.0.1:27017/NutritionAssistant

PORT=5000

JWT_SECRET=yourSecretKey
```

---

# ▶ Running the Application

## Start Backend

```bash
cd server

npm run dev
```

or

```bash
node server.js
```

---

## Start Frontend

```bash
cd client

npm run dev
```

---

# 🌐 Application URLs

Frontend

```
http://localhost:5173
```

Backend

```
http://localhost:5000
```

MongoDB

```
mongodb://127.0.0.1:27017
```

---

# 🔄 Application Workflow

```
User
   │
   ▼
React Frontend
   │
   ▼
Axios API Calls
   │
   ▼
Express REST APIs
   │
   ▼
Controllers
   │
   ▼
Mongoose Models
   │
   ▼
MongoDB Database
   │
   ▼
JSON Response
   │
   ▼
React UI Updates
```

---

# 📁 Folder Structure

## Client

- assets/
- components/
- pages/
- services/
- App.jsx
- main.jsx

## Server

- config/
- controllers/
- middleware/
- models/
- routes/
- server.js

---

# 📌 Main Modules

- User Authentication
- Meal Planner
- Food Search
- BMI Calculator
- Calorie Calculator
- Nutrition Recommendations
- Daily Nutrition Tracking
- User Dashboard
- Profile Management

---

# 🔒 Security Features

- JWT Authentication
- Password Hashing using bcryptjs
- Protected API Routes
- Environment Variables
- Input Validation

---

# 🚀 Future Enhancements

- AI-powered Diet Recommendations
- Barcode Food Scanner
- Nutrition Chatbot
- Fitness Tracker Integration
- Doctor Consultation Module
- Mobile Application
- Push Notifications
- Voice Assistant Support

---

# 📚 Documentation

The repository contains detailed documentation for every development stage:

- Project Setup
- User Flow
- MVC Pattern
- Technical Architecture
- Frontend Structure
- Backend Structure
- Configure MongoDB
- Create Database Connection
- Create Schemas and Models
- Development and Explanation
- Steps for Execution

---

# 🎯 Expected Outcome

The Nutrition Assistant application enables users to maintain a healthy lifestyle through efficient meal planning, calorie tracking, nutrition analysis, and personalized diet recommendations. The MERN Stack architecture ensures a scalable, secure, and maintainable full-stack web application.

---

# 👨‍💻 Authors

- **SURESHBABU REDDY**
- **BATTULA HAREESH**
- **NARRA KOTESWARARAO**
- **GOPI CHAND THUMMALA**
- **RAJESH SINGOTHU**

---

# 📄 License

This project is developed for educational and learning purposes as part of a **MERN Stack Full-Stack Development Project**.

---

## ⭐ If you found this project useful, consider giving it a star on GitHub!
