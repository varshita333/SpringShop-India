# SpringShop-India E-commerce Application

A full-stack, production-ready e-commerce platform built specifically for the Indian market, featuring Spring Boot 3, React 18, and MySQL.

## Features

- **JWT Authentication**: Secure login and registration.
- **Role-Based Access**: ADMIN and USER roles.
- **Product Management**: Browse, search, and manage products.
- **Cart System**: Persistent local storage cart with quantity management.
- **Responsive UI**: Built with Tailwind CSS, optimized for mobile and desktop.
- **Secure Backend**: REST API with Spring Security 6 and JPA.
- **Auto-Seeded Data**: Initial admin user and products are created automatically on first run.

## Prerequisites

- **Java**: JDK 17 or higher
- **Node.js**: v18 or higher
- **MySQL**: Running on port 3306
- **Maven**: (Optional, uses mvnw)

## Getting Started

### 1. Database Setup

1. Start your MySQL server.
2. Create a database named `springshop_db` or let the application create it automatically.
3. Update `backend/src/main/resources/application.properties` with your database username and password.

### 2. Run the Backend

1. Navigate to the `backend/` directory:
    cd backend
2. Run the application:
    ./mvnw spring-boot:run
3. The server will start at `http://localhost:8080`.
4. Swagger API documentation is available at `http://localhost:8080/swagger-ui/index.html`.

### 3. Run the Frontend

1. Navigate to the `frontend/` directory:
    cd frontend
2. Install dependencies:
    npm install
3. Start the React development server:
    npm start
4. The application will open at `http://localhost:3000`.

## Default Credentials

The application automatically seeds an admin user on startup:
- **Email**: `admin@springshop.com`
- **Password**: `admin123`
- **Role**: ADMIN

## Project Structure

- `backend/`: Spring Boot Maven project
    - `config/`: Security, JWT, and App configurations
    - `controller/`: REST endpoints
    - `model/`: JPA entities
    - `repository/`: Data access layer
    - `service/`: Business logic
    - `dto/`: Data Transfer Objects
- `frontend/`: React application
    - `src/context/`: Auth and Cart state management
    - `src/services/`: API integration using Axios
    - `src/components/`: Reusable UI components
    - `src/pages/`: Main views (Home, Login, Cart)

## Troubleshooting

- **CORS Errors**: Ensure the React app is running on `http://localhost:3000`. The backend is configured to allow this origin.
- **Database Connection**: If the app fails to start, verify your MySQL service is running and credentials in `application.properties` are correct.
- **Port Conflict**: If port 8080 or 3000 is occupied, change them in `application.properties` (backend) or `.env` (frontend).
