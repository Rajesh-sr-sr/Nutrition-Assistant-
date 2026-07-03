# FRONTEND STRUCTURE

## Project Name

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**React.js, Vite, Bootstrap, Axios, JavaScript (MERN Stack)**

---

# Objective

The frontend directory structure of the Nutrition Assistant application defines the organization of the React.js client application. It separates reusable UI components, application pages, API services, assets, and routing configuration into independent folders. This modular architecture improves code readability, maintainability, scalability, and simplifies frontend development.

---

# Frontend Technology Stack

* **React.js** – JavaScript library for building interactive user interfaces.
* **Vite** – Fast development server and build tool for React applications.
* **Bootstrap** – Responsive CSS framework for modern UI design.
* **Axios** – HTTP client used for communicating with backend REST APIs.
* **React Router DOM** – Enables navigation between application pages.
* **JavaScript (ES6+)** – Programming language used for frontend logic.

---

# Frontend Folder Structure

The following is the directory structure of the **Client** folder.

```text
Client/
│
├── package.json               # Frontend dependencies
├── vite.config.js             # Vite configuration
├── index.html                 # Root HTML page
│
├── public/                    # Static resources
│
├── src/
│   ├── assets/                # Images, icons, logos
│   ├── components/            # Reusable UI components
│   ├── pages/                 # Application pages
│   ├── services/              # Axios API services
│   ├── App.jsx                # Main React component
│   ├── main.jsx               # Application entry point
│   └── index.css              # Global styles
│
└── node_modules/              # Installed packages
```

---

# Subdirectory Explanations

## `main.jsx` (Application Entry Point)

Acts as the starting point of the React application.

**Responsibilities**

* Renders the App component.
* Loads global CSS.
* Initializes React Router.
* Mounts the application to the DOM.

---

## `App.jsx`

Acts as the root component of the application.

**Responsibilities**

* Defines application routes.
* Loads common layouts.
* Manages page rendering.
* Connects reusable components.

---

## `assets/`

Stores static resources.

### Contains

* Logo
* Images
* Icons
* Background Images
* Fonts

---

## `components/`

Contains reusable React components shared across multiple pages.

### Example Components

* Navbar.jsx
* Footer.jsx
* ProtectedRoute.jsx
* MealCard.jsx
* NutritionCard.jsx
* BMIForm.jsx
* Loading.jsx

---

## `pages/`

Contains all application screens.

### Example Pages

* Home.jsx
* Login.jsx
* Register.jsx
* Dashboard.jsx
* Profile.jsx
* MealPlanner.jsx
* FoodSearch.jsx
* NutritionCalculator.jsx
* DailyTracker.jsx
* Recommendations.jsx

---

## `services/`

Contains API service files responsible for backend communication.

### Responsibilities

* User Authentication API
* Meal API
* Nutrition API
* Food Search API
* Profile API

---

## `public/`

Stores static files served directly by the web server.

### Examples

* favicon.ico
* Images
* manifest.json

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

# Frontend Structure Diagram

```text
                    CLIENT (React Frontend)
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
     assets/          components/          pages/
        │                  │                  │
   Images, Icons     Reusable UI       Application Pages
        │                  │                  │
        └──────────────┬───┴──────────────────┘
                       │
                  App.jsx (Routes)
                       │
                  React Router
                       │
                  services/
                       │
                     Axios
                       │
               Express REST APIs
                       │
                    MongoDB
```

---

# Responsibilities of Frontend

### Components

* Reusable UI elements
* Navigation
* Forms
* Cards

### Pages

* User Interface
* Dashboard
* Authentication
* Meal Planning
* Nutrition Tracking

### Services

* API communication
* Authentication
* CRUD operations

### Assets

* Images
* Icons
* Static resources

---

# Advantages

* Modular folder organization.
* Reusable React components.
* Easy maintenance.
* Fast development using Vite.
* Responsive UI with Bootstrap.
* Efficient API communication using Axios.
* Scalable frontend architecture.
* Improved code readability.

---

# Expected Outcome

Successfully designed the **Frontend Structure** of the **Nutrition Assistant** application using **React.js** and **Vite**. The modular organization of pages, components, services, and assets enables efficient development, reusable code, responsive user interfaces, and seamless communication with the backend APIs.

---

## Project

**Nutrition Assistant – Personalized Nutrition Management System**

## Technology Stack

**MERN Stack (MongoDB, Express.js, React.js, Node.js)**
