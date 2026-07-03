# Nutrition Assistant - Entity Relationship (ER) Diagram

## Overview

The Nutrition Assistant is a MERN Stack based web application that helps users maintain a healthy lifestyle through personalized nutrition recommendations, meal planning, calorie tracking, and diet management.

The database is designed using multiple entities that are interconnected through one-to-many and many-to-many relationships. These entities store user details, meals, food information, diet plans, and daily nutrition logs.

---

# Entities

## 1. User

Description:

The User entity stores the information of registered users who access the Nutrition Assistant application.

Attributes

- user_id (Primary Key)
- full_name
- email
- password
- age
- gender
- height
- weight
- fitness_goal
- created_at

---

## 2. Meal

Description:

The Meal entity stores meals created by users for breakfast, lunch, dinner, or snacks.

Attributes

- meal_id (Primary Key)
- user_id (Foreign Key)
- meal_name
- meal_type
- calories
- protein
- carbohydrates
- fats
- meal_date

---

## 3. Food

Description:

The Food entity stores nutrition information for food items.

Attributes

- food_id (Primary Key)
- food_name
- category
- calories
- protein
- carbohydrates
- fats
- fiber

---

## 4. Diet Plan

Description

Stores personalized diet plans generated for users.

Attributes

- plan_id (Primary Key)
- user_id (Foreign Key)
- plan_name
- target_calories
- recommendation
- created_date

---

## 5. Nutrition Log

Description

Stores daily nutrition tracking information.

Attributes

- log_id (Primary Key)
- user_id (Foreign Key)
- meal_id (Foreign Key)
- total_calories
- water_intake
- exercise_minutes
- log_date

---

# Relationships

## User → Meal

Relationship

One User can create multiple Meals.

Cardinality

User (1) -------- (M) Meal

---

## User → Diet Plan

Relationship

One User can have multiple Diet Plans.

Cardinality

User (1) -------- (M) Diet Plan

---

## User → Nutrition Log

Relationship

One User maintains multiple Nutrition Logs.

Cardinality

User (1) -------- (M) Nutrition Log

---

## Meal → Food

Relationship

One Meal contains multiple Food Items.

One Food Item can belong to multiple Meals.

Cardinality

Meal (M) -------- (M) Food

This relationship can be implemented using a junction table named Meal_Food.

---

# ER Diagram (Text Representation)

                         +----------------------+
                         |        USER          |
                         +----------------------+
                         | user_id (PK)         |
                         | full_name            |
                         | email                |
                         | password             |
                         | age                  |
                         | gender               |
                         | height               |
                         | weight               |
                         | fitness_goal         |
                         +----------------------+
                                   |
             -------------------------------------------------
             |                     |                         |
             |                     |                         |
             V                     V                         V

      +----------------+   +-------------------+    +----------------------+
      |      MEAL      |   |    DIET PLAN      |    |   NUTRITION LOG      |
      +----------------+   +-------------------+    +----------------------+
      | meal_id (PK)   |   | plan_id (PK)      |    | log_id (PK)          |
      | user_id (FK)   |   | user_id (FK)      |    | user_id (FK)         |
      | meal_name      |   | plan_name         |    | meal_id (FK)         |
      | meal_type      |   | target_calories   |    | total_calories       |
      | calories       |   | recommendation    |    | water_intake         |
      | protein        |   | created_date      |    | exercise_minutes     |
      | carbohydrates  |   +-------------------+    | log_date             |
      | fats           |                            +----------------------+
      | meal_date      |
      +----------------+
              |
              |
              |
              V

      +-----------------------+
      |        FOOD           |
      +-----------------------+
      | food_id (PK)          |
      | food_name             |
      | category              |
      | calories              |
      | protein               |
      | carbohydrates         |
      | fats                  |
      | fiber                 |
      +-----------------------+

---

# Data Flow

1. User registers or logs into the application.
2. User creates meal entries.
3. Meals contain one or more food items.
4. Nutrition information is calculated from food items.
5. Daily nutrition logs are generated.
6. Personalized diet plans are created based on user goals.
7. User dashboard displays calorie intake and nutrition reports.

---

# Database Tables

1. Users
2. Meals
3. Foods
4. DietPlans
5. NutritionLogs

---

# Primary Keys

Users
- user_id

Meals
- meal_id

Foods
- food_id

DietPlans
- plan_id

NutritionLogs
- log_id

---

# Foreign Keys

Meals
- user_id

DietPlans
- user_id

NutritionLogs
- user_id
- meal_id

---

# Advantages of the ER Design

- Eliminates data redundancy
- Supports efficient CRUD operations
- Maintains data integrity
- Simplifies meal tracking
- Enables personalized diet recommendations
- Easy to extend with new modules
- Supports scalable MERN architecture
