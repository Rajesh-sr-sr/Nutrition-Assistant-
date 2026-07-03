# CREATE SCHEMAS AND MODELS

## Project Name

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**Node.js, Express.js, MongoDB, Mongoose (MERN Stack)**

---

# Objective

The Models layer defines the structure of the data stored in MongoDB using **Mongoose Schemas**. Each schema represents a collection in the database and specifies the fields, data types, validation rules, and relationships between documents. This ensures data consistency and enables efficient CRUD operations throughout the Nutrition Assistant application.

---

# Why Schemas and Models?

Schemas provide a blueprint for how data is stored in MongoDB. Models are created from these schemas and are used by controllers to perform database operations such as creating, reading, updating, and deleting records.

---

# Step 1: Create Models Folder

Inside the **server** directory, create a folder named **models**.

```text
Server/
│
├── models/
```

---

# Step 2: Create Model Files

Inside the **models** folder, create the following files:

```text
Server/
│
├── models/
│   ├── UserModel.js
│   ├── MealModel.js
│   ├── FoodModel.js
│   ├── NutritionModel.js
│   └── DailyLogModel.js
```

---

# UserModel.js

Stores user profile and authentication information.

### Fields

- Full Name
- Email Address
- Password
- Age
- Gender
- Height
- Weight
- Activity Level
- Fitness Goal
- Created Date

### Responsibilities

- User registration
- Login authentication
- Profile management
- Account information storage

---

# MealModel.js

Stores meals logged by users.

### Fields

- User ID
- Meal Name
- Meal Type
- Serving Size
- Calories
- Protein
- Carbohydrates
- Fat
- Meal Date

### Responsibilities

- Add meals
- Update meals
- Delete meals
- View meal history

---

# FoodModel.js

Maintains the nutrition database for available food items.

### Fields

- Food Name
- Category
- Calories
- Protein
- Carbohydrates
- Fat
- Fiber
- Sugar
- Serving Size

### Responsibilities

- Food search
- Nutrition lookup
- Food database management

---

# NutritionModel.js

Stores calculated nutritional information.

### Fields

- User ID
- BMI
- BMR
- Daily Calories
- Protein Requirement
- Water Intake
- Recommendation Date

### Responsibilities

- BMI calculation
- Calorie calculation
- Nutrition analysis
- Diet recommendation

---

# DailyLogModel.js

Tracks the user's daily nutrition intake.

### Fields

- User ID
- Breakfast
- Lunch
- Dinner
- Snacks
- Total Calories
- Total Protein
- Total Carbohydrates
- Total Fat
- Date

### Responsibilities

- Daily meal tracking
- Nutrition summary
- Progress monitoring

---

# Model Workflow

```text
User Request
      │
      ▼
Controller
      │
      ▼
Mongoose Model
      │
      ▼
MongoDB Collection
      │
      ▼
Database Response
      │
      ▼
Controller
      │
      ▼
API Response
```

---

# Folder Structure

```text
Server/
│
├── models/
│   ├── UserModel.js
│   ├── MealModel.js
│   ├── FoodModel.js
│   ├── NutritionModel.js
│   └── DailyLogModel.js
```

---

# Responsibilities of Models

### UserModel

- Stores user account details
- Validates user information
- Encrypts passwords before saving

### MealModel

- Stores meal records
- Maintains nutritional values for each meal

### FoodModel

- Stores food database
- Provides nutrition information

### NutritionModel

- Stores BMI and calorie calculations
- Saves personalized nutrition recommendations

### DailyLogModel

- Maintains daily nutrition logs
- Tracks user progress over time

---

# Advantages

- Strong data validation using Mongoose schemas.
- Organized database collections.
- Simplifies CRUD operations.
- Easy integration with controllers.
- Supports scalable application development.
- Improves code readability and maintenance.
- Ensures consistent data storage.

---

# Expected Outcome

Successfully created the **Schemas** and **Models** for the **Nutrition Assistant** backend using **Mongoose**. These models define the application's database structure and provide a reliable foundation for user management, meal tracking, food information, nutrition calculations, and daily progress monitoring.

---

## Project

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**MERN Stack (MongoDB, Express.js, React.js, Node.js)**
