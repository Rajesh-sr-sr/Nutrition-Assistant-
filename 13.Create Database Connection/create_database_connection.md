# CREATE DATABASE CONNECTION

## Project Name

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**Node.js, Express.js, MongoDB (MERN Stack)**

---

# Objective

The database connection is one of the most important steps in backend development. This module establishes a secure connection between the Nutrition Assistant backend and the MongoDB database using Mongoose. A successful database connection allows the application to store and retrieve user information, meal records, nutrition data, and daily logs.

---

# Prerequisites

Before creating the database connection, ensure the following packages are installed:

```bash
npm install mongoose dotenv
```

---

# Step 1: Create Database Configuration File

Inside the **server/config** folder, create a new file:

```text
server/
│
└── config/
    └── db.js
```

This file contains the MongoDB connection logic.

---

# Step 2: Configure MongoDB Connection

Add the following code inside **config/db.js**.

```javascript
const mongoose = require("mongoose");

const connectDB = async () => {
    try {
        await mongoose.connect(process.env.MONGO_URI);

        console.log("MongoDB Connected Successfully");
    } catch (error) {
        console.error(error.message);
        process.exit(1);
    }
};

module.exports = connectDB;
```

---

# Step 3: Create Environment Variables

Inside the **server** folder, create a file named:

```text
.env
```

Add your MongoDB connection string.

```env
MONGO_URI=mongodb://127.0.0.1:27017/nutritionassistant
PORT=5000
JWT_SECRET=yourSecretKey
```

If using MongoDB Atlas:

```env
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/nutritionassistant
```

---

# Step 4: Import Database Connection

Open **server.js** and import the database configuration.

```javascript
const connectDB = require("./config/db");
```

Call the function before starting the server.

```javascript
connectDB();
```

---

# Step 5: Start the Backend Server

Run the server using:

```bash
npm run dev
```

or

```bash
node server.js
```

If everything is configured correctly, the terminal displays:

```text
MongoDB Connected Successfully
Server running on Port 5000
```

---

# Database Connection Workflow

```text
Application Starts
        │
        ▼
Load Environment Variables (.env)
        │
        ▼
Read MongoDB Connection String
        │
        ▼
config/db.js
        │
        ▼
Mongoose.connect()
        │
        ▼
MongoDB Database
        │
        ▼
Connection Successful
        │
        ▼
Express Server Starts
```

---

# File Structure

```text
Server/
│
├── config/
│   └── db.js
│
├── .env
│
├── server.js
│
└── package.json
```

---

# Responsibilities of db.js

- Establishes the connection with MongoDB.
- Uses Mongoose as the Object Data Modeling (ODM) library.
- Reads the database URL from environment variables.
- Handles database connection errors.
- Prevents the server from running if the database connection fails.
- Exports the connection function for use in the application.

---

# Advantages

- Secure database connection using environment variables.
- Centralized database configuration.
- Easy to maintain and update.
- Supports both MongoDB Local and MongoDB Atlas.
- Improves scalability and code organization.
- Prevents application startup when the database is unavailable.

---

# Expected Outcome

Successfully connected the **Nutrition Assistant** backend application to **MongoDB** using **Mongoose**. The application is now capable of storing and retrieving user profiles, meal plans, nutrition information, calorie tracking records, and other application data through a secure and reliable database connection.

---

**Project:** Nutrition Assistant – Personalized Nutrition Management System

**Technology Stack:** MERN Stack (MongoDB, Express.js, React.js, Node.js)
