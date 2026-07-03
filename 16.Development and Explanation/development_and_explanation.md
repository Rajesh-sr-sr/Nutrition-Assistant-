# DEVELOPMENT AND EXPLANATION

## Project Name

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**React.js, Vite, Bootstrap, Axios, JavaScript (MERN Stack)**

---

# Objective

The frontend of the Nutrition Assistant application is developed using **React.js** and follows a modular folder structure. Each folder and component has a specific responsibility, making the application scalable, reusable, and easy to maintain. The frontend communicates with the backend REST APIs using Axios and provides users with an interactive interface for nutrition management.

---

# Frontend Directory Structure

```text
Client/
│
├── node_modules/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
│
├── package.json
└── vite.config.js
```

---

# Development and Explanation

## 1. Client Folder (`client/`)

The **client** folder contains the complete React.js frontend application.

**Responsibilities**

- User Interface
- Routing
- API Communication
- State Management
- Responsive Design

---

## 2. node_modules/

Contains all installed project dependencies.

Examples include:

- React
- React DOM
- React Router DOM
- Axios
- Bootstrap
- Vite

---

## 3. public/

Stores static files that are served directly by the web server.

Examples

- favicon.ico
- Images
- Logos
- Static Assets

---

## 4. src/

Contains the complete source code of the application.

Inside **src/**:

### assets/

Stores application resources.

Examples

- Images
- Icons
- Backgrounds
- Fonts

---

### components/

Contains reusable React components used across multiple pages.

Examples

#### Navbar.jsx

Navigation bar displayed throughout the application.

#### Footer.jsx

Displays footer information.

#### MealCard.jsx

Displays meal information.

#### NutritionCard.jsx

Displays nutrition statistics.

#### BMIForm.jsx

BMI calculator form.

#### ProtectedRoute.jsx

Protects authenticated pages.

---

### pages/

Contains all application pages.

#### Home.jsx

Landing page of the application.

#### Login.jsx

User login page.

#### Register.jsx

User registration page.

#### Dashboard.jsx

Displays user dashboard.

#### Profile.jsx

Shows user profile information.

#### MealPlanner.jsx

Allows users to create and manage meal plans.

#### FoodSearch.jsx

Searches foods from the nutrition database.

#### NutritionCalculator.jsx

Calculates BMI, BMR, and calorie requirements.

#### DailyTracker.jsx

Tracks daily calorie and nutrition intake.

#### Recommendations.jsx

Displays personalized nutrition recommendations.

---

### services/

Contains API communication logic.

Example files

- authService.js
- mealService.js
- nutritionService.js
- foodService.js
- profileService.js

Responsibilities

- Send HTTP requests
- Receive JSON responses
- Handle API errors
- Connect frontend with backend

---

## 5. App.jsx

Main React component.

Responsibilities

- Defines application routes.
- Loads pages.
- Connects common components.
- Manages application layout.

---

## 6. main.jsx

Application entry point.

Responsibilities

- Creates the React application.
- Renders App.jsx.
- Imports global CSS.
- Loads React Router.

---

## 7. index.css

Contains global CSS styles.

Responsibilities

- Common typography
- Colors
- Responsive styling
- Layout formatting

---

# Frontend Workflow

```text
User
   │
   ▼
React Components
   │
   ▼
React Router
   │
   ▼
Axios Services
   │
   ▼
Express REST APIs
   │
   ▼
MongoDB Database
   │
   ▼
JSON Response
   │
   ▼
React Components
   │
   ▼
Updated User Interface
```

---

# Advantages

- Modular folder organization.
- Reusable React components.
- Easy maintenance.
- Scalable architecture.
- Fast development using Vite.
- Responsive Bootstrap UI.
- Efficient API communication.
- Better code readability.

---

# Expected Outcome

Successfully developed and organized the frontend structure of the **Nutrition Assistant** application using **React.js**, **Vite**, and **Bootstrap**. The modular architecture enables efficient development, reusable components, responsive user interfaces, and seamless integration with backend REST APIs.

---

## Project

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**MERN Stack (MongoDB, Express.js, React.js, Node.js)**
