# BACKEND STRUCTURE

## Project Name

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**Node.js, Express.js, MongoDB (MERN Stack)**

---

# Objective

The backend directory structure of the Nutrition Assistant application defines the organization of files and modules required to build and run the Node.js/Express.js REST APIs. By separating configurations (`config`), database schemas (`models`), business logic (`controllers`), API routes (`routes`), middleware (`middleware`), and the application entry point (`server.js`), the project follows the Model-View-Controller (MVC) architecture, resulting in a clean, scalable, and maintainable backend.

---

# Backend Technology Stack

* **Node.js** – JavaScript runtime environment for executing server-side code.
* **Express.js** – Lightweight framework for building RESTful APIs.
* **MongoDB** – NoSQL database for storing user, meal, and nutrition information.
* **Mongoose** – ODM (Object Data Modeling) library for MongoDB.
* **JWT (JSON Web Token)** – Secure user authentication and authorization.
* **bcryptjs** – Password encryption using secure hashing algorithms.
* **dotenv** – Environment variable management.
* **Cors** – Enables secure communication between frontend and backend.

---

# Backend Folder Structure

Below is the directory structure of the backend **Server** folder.

```text
Server/
│
├── package.json              # Backend dependencies
├── server.js                 # Express application entry point
│
├── config/
│   └── db.js                 # MongoDB database connection
│
├── models/
│   ├── UserModel.js          # User information schema
│   ├── MealModel.js          # Meal details schema
│   ├── FoodModel.js          # Food items schema
│   ├── NutritionModel.js     # Nutrition information schema
│   └── DailyLogModel.js      # Daily calorie tracking schema
│
├── controllers/
│   ├── UserController.js
│   ├── MealController.js
│   ├── FoodController.js
│   ├── NutritionController.js
│   └── DailyLogController.js
│
├── routes/
│   ├── userRoutes.js
│   ├── mealRoutes.js
│   ├── foodRoutes.js
│   ├── nutritionRoutes.js
│   └── dailyLogRoutes.js
│
├── middleware/
│   ├── authMiddleware.js
│   └── errorMiddleware.js
│
└── node_modules/
```

---

# Subdirectory Explanations

## `server.js` (Server Initialization)

Acts as the entry point of the backend application.

**Responsibilities**

* Initializes the Express server.
* Connects to MongoDB.
* Registers middleware.
* Loads API routes.
* Starts the application on the configured server port.

---

## Models Folder (`models/`)

Stores all Mongoose schemas used by the application.

### UserModel

Stores user registration details.

* Name
* Email
* Password
* Age
* Height
* Weight
* Gender
* Activity Level

### MealModel

Stores user meal information.

* Meal Name
* Meal Type
* Calories
* Serving Size
* User Reference

### FoodModel

Contains food database information.

* Food Name
* Calories
* Protein
* Carbohydrates
* Fat
* Fiber

### NutritionModel

Stores nutritional calculations.

* BMI
* Daily Calories
* Protein Requirement
* Water Intake

### DailyLogModel

Stores daily nutrition logs.

* Meals Consumed
* Calories
* Protein
* Carbohydrates
* Fat
* Date

---

## Controllers Folder (`controllers/`)

Contains the business logic for processing incoming API requests.

**Responsibilities**

* Validate user input.
* Process authentication.
* Calculate BMI and calorie requirements.
* Manage meal plans.
* Retrieve nutrition information.
* Generate personalized recommendations.
* Process CRUD operations.

---

## Routes Folder (`routes/`)

Maps HTTP requests to controller functions.

### Sample API Routes

* `POST /api/users/register` → Register new users.
* `POST /api/users/login` → Authenticate users.
* `GET /api/users/profile` → Retrieve user profile.
* `POST /api/meals/add` → Add meal.
* `GET /api/meals` → View meal history.
* `POST /api/nutrition/calculate` → Calculate BMI and calories.
* `GET /api/recommendations` → Get personalized diet suggestions.

---

## Middleware Folder (`middleware/`)

Contains reusable middleware functions.

### authMiddleware

* Verifies JWT tokens.
* Protects private routes.
* Adds authenticated user details to the request.

### errorMiddleware

* Handles application errors.
* Returns standardized API responses.

---

## Config Folder (`config/`)

Contains project configuration files.

### db.js

* Connects the application to MongoDB.
* Configures Mongoose connection settings.
* Handles database connection errors.

---

# Backend API Workflow

The following diagram illustrates how an API request is processed within the Nutrition Assistant backend.

```mermaid
sequenceDiagram
    autonumber

    actor User as React Frontend

    participant Route as Express Routes

    participant Auth as Authentication Middleware

    participant Controller as Controllers

    participant Model as Mongoose Models

    database MongoDB

    User->>Route: API Request
    Route->>Auth: Verify JWT Token

    Auth-->>Route: Authentication Success

    Route->>Controller: Execute Business Logic

    Controller->>Model: Database Operation

    Model->>MongoDB: Read / Write Data

    MongoDB-->>Model: Database Response

    Model-->>Controller: Return Data

    Controller-->>User: JSON Response
```

---

# Structural Advantages

* **Modular Architecture** – Keeps models, controllers, routes, and middleware separated.
* **Scalable Design** – Easy to add new nutrition modules and APIs.
* **Secure Authentication** – JWT protects private user resources.
* **Reusable Components** – Middleware and controllers reduce code duplication.
* **Easy Maintenance** – Organized project structure improves readability.
* **MVC Pattern** – Separates business logic from routing and data management.
* **Database Flexibility** – MongoDB easily stores structured and semi-structured nutrition data.

---

# Expected Outcome

Successfully designed the backend structure of the **Nutrition Assistant** application using **Node.js**, **Express.js**, **MongoDB**, and the **MVC architectural pattern**. The backend supports secure authentication, nutrition management, meal tracking, calorie calculations, and scalable RESTful API development while maintaining a clean and maintainable codebase.

---

**Project:** Nutrition Assistant – Personalized Nutrition Management System

**Technology Stack:** MERN Stack (MongoDB, Express.js, React.js, Node.js)
