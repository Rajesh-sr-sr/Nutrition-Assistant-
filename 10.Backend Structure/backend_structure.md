# Backend Structure

## Project Overview

The **Nutrition Assistant – Personalized Nutrition Management System** backend is developed using the **MERN Stack** (MongoDB, Express.js, React.js, and Node.js). It provides RESTful APIs for user authentication, nutrition management, meal tracking, calorie calculations, and daily nutrition logging.

The project follows the **Model-View-Controller (MVC)** architecture to ensure a modular, scalable, and maintainable codebase. Application components are organized into separate folders for configuration, database models, controllers, routes, and middleware, making development and future enhancements easier.

---

# Technology Stack

* **Node.js** – Server-side JavaScript runtime.
* **Express.js** – Framework for building RESTful APIs.
* **MongoDB** – NoSQL database for storing application data.
* **Mongoose** – ODM library for MongoDB.
* **JWT (JSON Web Token)** – User authentication and route protection.
* **bcryptjs** – Password hashing for secure authentication.
* **dotenv** – Environment variable management.
* **CORS** – Enables secure communication between frontend and backend.

---

# Backend Directory Structure

```text
Server/
│
├── package.json              # Backend dependencies
├── server.js                 # Application entry point
│
├── config/
│   └── db.js                 # MongoDB connection configuration
│
├── models/
│   ├── UserModel.js          # User schema
│   ├── MealModel.js          # Meal schema
│   ├── FoodModel.js          # Food schema
│   ├── NutritionModel.js     # Nutrition schema
│   └── DailyLogModel.js      # Daily nutrition log schema
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

# Folder Description

## `server.js`

The main entry point of the backend application.

**Responsibilities**

* Initialize the Express server.
* Connect to MongoDB.
* Configure middleware.
* Register API routes.
* Start the server on the configured port.

---

## `config/`

Contains application configuration files.

### `db.js`

Responsible for:

* Connecting to MongoDB using Mongoose.
* Managing database connection settings.
* Handling connection errors.

---

## `models/`

Contains all Mongoose schemas used in the application.

### UserModel

Stores user information such as:

* Name
* Email
* Password (hashed)
* Age
* Height
* Weight
* Gender
* Activity Level

### MealModel

Stores meal-related information including:

* Meal Name
* Meal Type
* Calories
* Serving Size
* User Reference

### FoodModel

Maintains the food database with nutritional values.

* Food Name
* Calories
* Protein
* Carbohydrates
* Fat
* Fiber

### NutritionModel

Stores calculated nutrition data.

* BMI
* Daily Calorie Requirement
* Protein Requirement
* Daily Water Intake

### DailyLogModel

Maintains users' daily nutrition records.

* Meals Consumed
* Calories
* Protein
* Carbohydrates
* Fat
* Date

---

## `controllers/`

Contains the business logic for processing API requests.

Responsibilities include:

* User authentication
* Input validation
* BMI and calorie calculations
* Meal management
* Nutrition calculations
* CRUD operations
* Personalized nutrition recommendations

---

## `routes/`

Defines API endpoints and maps requests to controller functions.

### Sample Endpoints

| Method | Endpoint                   | Description                                |
| ------ | -------------------------- | ------------------------------------------ |
| POST   | `/api/users/register`      | Register a new user                        |
| POST   | `/api/users/login`         | Authenticate a user                        |
| GET    | `/api/users/profile`       | Retrieve user profile                      |
| POST   | `/api/meals/add`           | Add a meal                                 |
| GET    | `/api/meals`               | Get meal history                           |
| POST   | `/api/nutrition/calculate` | Calculate BMI and calorie requirements     |
| GET    | `/api/recommendations`     | Get personalized nutrition recommendations |

---

## `middleware/`

Contains reusable middleware components.

### `authMiddleware`

* Verifies JWT tokens.
* Protects private routes.
* Attaches authenticated user information to requests.

### `errorMiddleware`

* Handles application errors.
* Returns standardized JSON error responses.
* Improves API consistency.

---

# API Request Flow

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
    Route->>Auth: Verify JWT

    Auth-->>Route: Authentication Successful

    Route->>Controller: Execute Business Logic
    Controller->>Model: Perform Database Operation

    Model->>MongoDB: Read / Write Data
    MongoDB-->>Model: Return Result

    Model-->>Controller: Return Data
    Controller-->>User: JSON Response
```

---

# Key Features

* Modular MVC architecture
* RESTful API design
* Secure JWT authentication
* Password hashing using bcrypt
* MongoDB integration with Mongoose
* Meal and nutrition management
* BMI and calorie calculations
* Daily nutrition tracking
* Reusable middleware components
* Scalable and maintainable project structure

---

# Benefits

* Clean separation of concerns through MVC.
* Easy to maintain and extend.
* Secure authentication and authorization.
* Organized project structure for collaborative development.
* Simplified database management using Mongoose.
* Flexible architecture for adding future nutrition-related features.

---

# Outcome

The backend provides a robust foundation for the **Nutrition Assistant – Personalized Nutrition Management System**, enabling secure user authentication, nutrition calculations, meal management, daily nutrition tracking, and scalable RESTful API development while maintaining a clean and well-organized project architecture.
