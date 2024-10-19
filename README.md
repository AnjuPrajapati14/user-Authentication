# User-Authentication Crypto Platform (MERN Stack)

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Technologies](#technologies)
- [Installation](#installation)
- [Backend Setup](#backend-setup)
- [Frontend Setup](#frontend-setup)
- [API Endpoints](#api-endpoints)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction
**Crypto app** is a basic fintech platform built using the MERN stack (MongoDB, Express, React, Node.js) with additional technologies such as **Hasura** for GraphQL APIs, **JWT** for authentication, and **Chakra UI** for frontend components. The project involves handling user authentication, transactions, and various fintech-related functionalities.

## Features
- User Authentication (Signup, Signin, JWT-based sessions)
- Email verification and password reset flows
- Transaction management (add, view, and manage transactions)
- Responsive and accessible design using Chakra UI
- API integration with Hasura for handling data
- Form validation and error handling using Mongoose

## Technologies
- **Frontend**: React, Chakra UI, React Query, Axios
- **Backend**: Node.js, Express.js, MongoDB, Mongoose, Hasura (GraphQL)
- **Authentication**: JWT (JSON Web Token), Nodemailer for email
- **Other**: Postman (for API testing), React Router (for navigation)

---

## Installation

### Prerequisites
- **Node.js** installed on your system
- **MongoDB** installed or available via cloud services (e.g., MongoDB Atlas)
- **Hasura** (if used for GraphQL)
- **Postman** (optional for API testing)

### Backend Setup
1. Clone the repository from GitHub:
    ```bash
    git clone https://github.com/yourusername/project.git
    ```

2. Navigate to the backend folder:
    ```bash
    cd project-7/backend
    ```

3. Install backend dependencies:
    ```bash
    npm install
    ```

4. Set up environment variables by creating a `.env` file:
    ```plaintext
    MONGO_URI=<your-mongo-uri>
    JWT_KEY=<your-jwt-secret>
    FRONTEND_URL=http://localhost:3000
    EMAIL_USER=<your-email>
    EMAIL_PASS=<your-email-password>
    ```

5. Start the backend server:
    ```bash
    npm start
    ```

6. The backend will run on `http://localhost:5000`.

### Frontend Setup
1. Navigate to the frontend folder:
    ```bash
    cd project-7/frontend
    ```

2. Install frontend dependencies:
    ```bash
    yarn install
    ```

3. Start the frontend development server:
    ```bash
    yarn start
    ```

4. The frontend will run on `http://localhost:3000`.

---

## API Endpoints

### Authentication
- **POST** `/api/auth/signup`: User signup
- **POST** `/api/auth/signin`: User login
- **POST** `/api/auth/forgot-password`: Send password reset email
- **POST** `/api/auth/verify-email`: Verify email after signup

### Transactions
- **GET** `/api/transactions`: Get all transactions
- **POST** `/api/transactions`: Add a new transaction
- **PUT** `/api/transactions/:id`: Update a transaction
- **DELETE** `/api/transactions/:id`: Delete a transaction

---

## Folder Structure
```plaintext
project/
│
├── backend/                # Node.js + Express backend
│   ├── controllers/        # API controllers for authentication, transactions, etc.
│   ├── models/             # Mongoose models
│   ├── routes/             # API routes
│   ├── utils/              # Utility functions (e.g., email, token handling)
│   ├── .env                # Environment variables (local setup)
│   └── server.js           # Entry point for the backend server
│
├── frontend/               # React frontend
│   ├── components/         # React components (e.g., forms, buttons, etc.)
│   ├── pages/              # Application pages (e.g., login, dashboard, etc.)
│   ├── services/           # API service calls using Axios
│   ├── App.js              # Main app entry
│   ├── index.js            # Entry point for React
│   └── .env                # Environment variables for frontend
│
└── README.md               # Project readme file
