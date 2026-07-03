# Nutrition Assistant - MVC Pattern

## Overview

The Nutrition Assistant backend is developed using the **Model-View-Controller (MVC)** architectural pattern. MVC separates the application into three independent components—Model, View, and Controller—making the project more organized, scalable, maintainable, and easier to develop.

---

# MVC Architecture

```
                 User
                   |
                   |
             HTTP Request
                   |
                   v
              Routes (View)
                   |
                   v
             Controllers
                   |
        -----------------------
        |                     |
        v                     |
      Models                  |
        |                     |
        v                     |
     MongoDB Database <--------
                   |
                   v
            HTTP Response
                   |
                   v
                 User
```

---

# Model Layer (Data Layer)

The **Model** represents the application's data and business entities. It communicates directly with the MongoDB database using Mongoose.

### Responsibilities

- Define database schemas
- Store user information
- Store meal plans
- Store nutrition records
- Perform CRUD operations
- Validate data before saving

### Example Models

- User
- Meal
- FoodItem
- Nutrition
- DailyLog

### Technologies

- MongoDB
- Mongoose

---

# Controller Layer

The **Controller** acts as the bridge between the client requests and the database. It receives requests, processes business logic, interacts with models, and returns appropriate responses.

### Responsibilities

- User Registration
- User Login
- Authentication
- BMI Calculation
- Calorie Calculation
- Meal Management
- Nutrition Recommendation
- Food Logging
- Error Handling

### Example Controllers

- userController.js
- mealController.js
- nutritionController.js
- profileController.js

---

# View Layer (Routing/API Layer)

In a REST API, the **View** is represented by Express Routes that expose endpoints to the frontend.

### Responsibilities

- Receive HTTP Requests
- Define API Endpoints
- Call Controller Functions
- Return JSON Responses
- Handle Route Navigation

### Example Routes

```
POST /api/users/register

POST /api/users/login

GET /api/users/profile

PUT /api/users/profile

GET /api/meals

POST /api/meals

PUT /api/meals/:id

DELETE /api/meals/:id

POST /api/nutrition/calculate

GET /api/history
```

---

# Request Flow

### Step 1

User performs an action from the React frontend.

↓

### Step 2

React sends an HTTP request to the Express API.

↓

### Step 3

The Express Route receives the request.

↓

### Step 4

The Route calls the appropriate Controller.

↓

### Step 5

The Controller validates input and processes business logic.

↓

### Step 6

The Controller communicates with the Model.

↓

### Step 7

The Model performs database operations using MongoDB.

↓

### Step 8

The database returns the requested data.

↓

### Step 9

The Controller prepares the response.

↓

### Step 10

Express sends the JSON response back to the React frontend.

---

# Project Folder Structure (MVC)

```
backend
│
├── config
│
├── controllers
│   ├── userController.js
│   ├── mealController.js
│   ├── nutritionController.js
│   └── profileController.js
│
├── middleware
│   └── authMiddleware.js
│
├── models
│   ├── User.js
│   ├── Meal.js
│   ├── FoodItem.js
│   ├── Nutrition.js
│   └── DailyLog.js
│
├── routes
│   ├── userRoutes.js
│   ├── mealRoutes.js
│   ├── nutritionRoutes.js
│   └── profileRoutes.js
│
├── server.js
└── package.json
```

---

# Advantages of MVC

- Clear separation of application layers
- Easy to maintain and update
- Better code organization
- Reusable business logic
- Simplified debugging
- Improved scalability
- Secure API development
- Faster team collaboration

---

# Technologies Used

- MongoDB
- Mongoose
- Express.js
- Node.js
- React.js
- JWT Authentication
- Axios

---

# Outcome

The MVC architecture enables the Nutrition Assistant application to:

- Maintain clean and modular code.
- Separate frontend and backend responsibilities.
- Securely manage user authentication.
- Handle nutrition and meal management efficiently.
- Scale easily as new features are added.
- Improve development and maintenance productivity.

---
