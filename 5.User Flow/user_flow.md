# Nutrition Assistant - User Flow

## Overview

The Nutrition Assistant application helps users maintain a healthy lifestyle by providing personalized nutrition guidance, calorie tracking, meal planning, and diet recommendations. The user flow below describes how users interact with the application from registration to tracking their nutritional progress.

---

# User Flow

## 1. User Registration

- User opens the Nutrition Assistant application.
- Selects **Sign Up**.
- Enters:
  - Full Name
  - Email Address
  - Password
  - Age
  - Gender
  - Height
  - Weight
  - Activity Level
- System validates the information.
- User account is created successfully.

---

## 2. User Login

- User enters registered email and password.
- System authenticates the credentials.
- JWT token is generated.
- User is redirected to the Dashboard.

---

## 3. Dashboard

After successful login, the dashboard displays:

- Daily calorie target
- BMI information
- Nutrition summary
- Today's meals
- Water intake
- Progress overview
- Quick navigation to all features

---

## 4. Profile Management

The user can:

- View profile
- Edit personal details
- Update height and weight
- Change activity level
- Update fitness goals
- Save profile changes

---

## 5. BMI & Calorie Calculation

User enters:

- Height
- Weight
- Age
- Gender
- Activity Level

System calculates:

- Body Mass Index (BMI)
- Basal Metabolic Rate (BMR)
- Daily Calorie Requirement

Results are displayed instantly.

---

## 6. Food Search

The user:

- Searches for a food item.
- Selects the desired food.
- Views nutrition details such as:
  - Calories
  - Protein
  - Carbohydrates
  - Fat
  - Fiber

---

## 7. Meal Planning

The user creates a meal plan by:

- Selecting breakfast
- Selecting lunch
- Selecting dinner
- Adding snacks
- Choosing serving quantity

The system stores the meal plan.

---

## 8. Daily Food Logging

The user logs consumed food items.

The application records:

- Food Name
- Quantity
- Calories
- Protein
- Carbohydrates
- Fat
- Date and Time

Daily nutrition totals are automatically updated.

---

## 9. Nutrition Recommendations

Based on:

- BMI
- Daily calorie intake
- Fitness goal
- Activity level

The system recommends:

- Healthy foods
- Meal suggestions
- Calorie intake adjustments
- Balanced nutrition tips

---

## 10. Progress Tracking

Users can monitor:

- Daily calorie intake
- Weekly progress
- BMI history
- Meal history
- Nutrition trends

Progress is displayed using charts and reports.

---

## 11. Logout

The user clicks **Logout**.

The application:

- Invalidates the user session.
- Removes the authentication token.
- Redirects to the Login page.

---

# User Flow Diagram

```
Start
   |
   v
Open Application
   |
   v
Register / Login
   |
   v
Authentication
   |
   v
Dashboard
   |
   +-------------------------+
   |                         |
   v                         v
Profile                 Food Search
   |                         |
   |                         v
   |                  View Nutrition
   |                         |
   +-----------+-------------+
               |
               v
        BMI & Calorie Calculator
               |
               v
         Meal Planning
               |
               v
        Daily Food Logging
               |
               v
  Nutrition Recommendations
               |
               v
      Progress Tracking
               |
               v
            Logout
               |
               v
              End
```

---

# User Journey Summary

1. Register a new account.
2. Login securely.
3. Complete profile information.
4. Calculate BMI and calorie requirements.
5. Search and select food items.
6. Create personalized meal plans.
7. Log daily food intake.
8. Receive nutrition recommendations.
9. Track health progress over time.
10. Logout securely.

---

# Technologies Used

- React.js
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT Authentication
- Axios
- HTML5
- CSS3
- JavaScript

---

# Outcome

The user flow ensures:

- Simple onboarding process
- Secure authentication
- Personalized nutrition management
- Easy meal planning
- Accurate calorie tracking
- Better health monitoring
- Smooth and intuitive user experience

---
