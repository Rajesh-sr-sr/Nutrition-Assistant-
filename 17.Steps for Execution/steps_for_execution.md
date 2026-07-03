# STEPS FOR EXECUTION

## Project Name

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**MERN Stack (MongoDB, Express.js, React.js, Node.js)**

---

# Objective

This document explains the step-by-step process for executing the Nutrition Assistant application. It covers starting both the frontend and backend servers, configuring the MongoDB database, and verifying that the application is running successfully.

---

# Prerequisites

Before running the project, ensure the following software is installed on your system:

- Node.js (v18 or above)
- npm (Node Package Manager)
- MongoDB Community Server or MongoDB Atlas
- Visual Studio Code
- Git (Optional)

---

# Step 1: Open the Project

1. Open **Visual Studio Code**.
2. Select **File → Open Folder**.
3. Open the **Nutrition-Assistant** project folder.

Project Structure

```text
Nutrition-Assistant/
│
├── client/
└── server/
```

---

# Step 2: Start the Frontend (React Application)

Open a terminal inside VS Code.

Navigate to the client folder.

```bash
cd client
```

Install all frontend dependencies (only the first time).

```bash
npm install
```

Start the React development server.

```bash
npm run dev
```

The frontend application will start on:

```text
http://localhost:5173
```

---

# Step 3: Start the Backend (Node.js & Express Server)

Open a **new terminal** in VS Code.

Navigate to the server folder.

```bash
cd server
```

Install backend dependencies (only the first time).

```bash
npm install
```

---

# Step 4: Configure Environment Variables

Inside the **server** folder, create a file named:

```text
.env
```

Add the following configuration.

### MongoDB Local

```env
MONGO_URI=mongodb://127.0.0.1:27017/NutritionAssistant
PORT=5000
JWT_SECRET=yourSecretKey
```

### MongoDB Atlas

```env
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/NutritionAssistant
PORT=5000
JWT_SECRET=yourSecretKey
```

---

# Step 5: Start the Backend Server

Run the backend server.

Using Nodemon

```bash
npm run dev
```

or using Node.js

```bash
node server.js
```

The backend server starts on:

```text
http://localhost:5000
```

Terminal Output

```text
MongoDB Connected Successfully
Server running on Port 5000
```

---

# Step 6: Verify Application

Open your browser.

Visit:

```text
http://localhost:5173
```

You should now see the **Nutrition Assistant** homepage.

---

# Execution Workflow

```text
Open Project
      │
      ▼
Start MongoDB
      │
      ▼
Run Backend Server
      │
      ▼
Backend Connects to MongoDB
      │
      ▼
Run React Frontend
      │
      ▼
Frontend Calls REST APIs
      │
      ▼
Express Server
      │
      ▼
MongoDB Database
      │
      ▼
JSON Response
      │
      ▼
Application Ready
```

---

# Default URLs

| Service | URL |
|----------|----------------------------|
| Frontend | http://localhost:5173 |
| Backend | http://localhost:5000 |
| MongoDB | mongodb://127.0.0.1:27017 |

---

# Troubleshooting

### If npm is not recognized

Check Node.js installation.

```bash
node -v
npm -v
```

---

### If MongoDB connection fails

- Ensure MongoDB service is running.
- Verify the **MONGO_URI** in the `.env` file.
- Restart the backend server.

---

### If Port 5173 or 5000 is already in use

Stop the application using that port or change the port number in the configuration.

---

# Expected Outcome

Successfully executed the **Nutrition Assistant** application by starting the frontend and backend servers, connecting to MongoDB, and launching the application in the browser. Users can now register, log in, manage meals, calculate nutrition values, and access personalized diet recommendations.

---

## Project

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**MERN Stack (MongoDB, Express.js, React.js, Node.js)**
