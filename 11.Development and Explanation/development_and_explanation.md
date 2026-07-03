# DEVELOPMENT AND EXPLANATION

## Project Name

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

Node.js, Express.js, MongoDB, Mongoose, JWT Authentication (MERN Stack)

---

# Objective

The backend of the Nutrition Assistant application is responsible for handling user authentication, nutrition calculations, meal management, food tracking, and communication with the MongoDB database. The application follows the Model-View-Controller (MVC) architecture to ensure clean code organization, modularity, scalability, and maintainability.

---

# Project Backend Structure

```
Server/
│
├── config/
├── controllers/
├── middleware/
├── models/
├── routes/
├── services/
├── utils/
├── server.js
└── package.json
```

---

# 1. Controllers/

Controllers contain the application's business logic. They receive requests from the routes, process the data, interact with the database models, and send responses back to the client.

### UserController.js

- Registers new users.
- Authenticates user login.
- Retrieves user profile information.
- Updates user profile.

### MealController.js

- Adds daily meals.
- Retrieves meal history.
- Updates meal information.
- Deletes meals.

### NutritionController.js

- Calculates BMI.
- Calculates daily calorie requirements.
- Performs nutrition analysis.

### FoodController.js

- Searches food items.
- Retrieves nutritional values.
- Manages food database operations.

### RecommendationController.js

- Generates personalized meal recommendations.
- Suggests healthy diet plans.
- Provides nutrition tips based on user goals.

---

# 2. Config/

Configuration files manage application settings.

### db.js

Responsibilities:

- Connects the application to MongoDB.
- Configures Mongoose connection.
- Handles database connection errors.
- Exports database connection.

---

# 3. Middleware/

Middleware functions execute before controller logic.

### authMiddleware.js

Responsibilities:

- Verifies JWT tokens.
- Protects private routes.
- Authenticates users.

### errorMiddleware.js

Responsibilities:

- Handles application exceptions.
- Returns standardized error responses.
- Prevents server crashes.

---

# 4. Models/

Models define MongoDB schemas using Mongoose.

### UserModel.js

Stores:

- Name
- Email
- Password
- Age
- Gender
- Height
- Weight
- Activity Level

### MealModel.js

Stores:

- Meal Name
- Meal Type
- Calories
- Protein
- Carbohydrates
- Fat

### FoodModel.js

Stores:

- Food Name
- Serving Size
- Nutrition Information

### NutritionModel.js

Stores:

- BMI
- Daily Calories
- Protein Requirement
- Water Intake

### RecommendationModel.js

Stores:

- Diet Plan
- Meal Suggestions
- Nutrition Recommendations

---

# 5. Routes/

Routes connect frontend requests with controller methods.

### userRoutes.js

Endpoints:

- POST /register
- POST /login
- GET /profile
- PUT /profile

### mealRoutes.js

Endpoints:

- POST /add
- GET /
- PUT /:id
- DELETE /:id

### nutritionRoutes.js

Endpoints:

- POST /calculate
- GET /summary

### foodRoutes.js

Endpoints:

- GET /search
- GET /food/:id

### recommendationRoutes.js

Endpoints:

- GET /recommendations

---

# 6. Services/

Service files contain reusable business logic.

### nutritionService.js

Responsibilities:

- BMI calculation
- Calorie calculation
- Nutrition analysis
- Diet recommendation logic

---

# 7. Utils/

Utility functions provide helper methods used across the application.

### calculator.js

Functions:

- BMI Formula
- BMR Formula
- Daily Calorie Formula
- Nutrition Calculations

---

# Entry Point – server.js

The server.js file is the starting point of the backend application.

Responsibilities:

- Initializes Express.js server.
- Connects to MongoDB.
- Loads middleware.
- Registers API routes.
- Starts server on specified port.
- Handles incoming HTTP requests.

---

# Backend Workflow

```
Client Request
        │
        ▼
Express Routes
        │
        ▼
Authentication Middleware
        │
        ▼
Controllers
        │
        ▼
Business Services
        │
        ▼
Mongoose Models
        │
        ▼
MongoDB Database
        │
        ▼
JSON Response
```

---

# Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT Authentication
- bcryptjs
- dotenv
- CORS

---

# Advantages

- Modular MVC Architecture
- Secure Authentication
- Organized Code Structure
- Easy API Development
- Efficient Database Management
- Reusable Business Logic
- Easy Maintenance
- Scalable Backend

---

# Expected Outcome

Successfully developed the backend architecture of the Nutrition Assistant application using Node.js, Express.js, MongoDB, and the MVC design pattern. The backend provides secure authentication, nutrition analysis, meal management, personalized diet recommendations, and efficient communication between the frontend and database.

---

**Project:** Nutrition Assistant – Personalized Nutrition Management System

**Technology Stack:** MERN Stack (MongoDB, Express.js, React.js, Node.js)
