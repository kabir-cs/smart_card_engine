# Backend

This is the backend for the Credit Card Recommender application. It is built using Spring Boot and MongoDB.

---

## Table of Contents
- [Overview](#overview)
- [Setup](#setup)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Security](#security)
- [Modifying the Application](#modifying-the-application)

---

## Overview
The backend provides RESTful APIs for user authentication, registration, and credit card data management. It uses MongoDB for data storage and BCrypt for secure password hashing.

## Setup
1. Ensure you have **Java 17** and **Maven** installed.
2. Navigate to the `backend` directory.
3. Start the application:
   ```bash
   ./mvnw spring-boot:run
   ```
4. The backend will run on [http://localhost:8080](http://localhost:8080) by default.

## Project Structure
- `model/` — Data models (e.g., `User`, `CreditCard`)
- `controller/` — REST controllers:
  - `UserController`: Handles registration and login
  - `CreditCardController`: Manages credit card data
  - `HelloController`: Simple test endpoint
- `repository/` — MongoDB repositories
- `config/` — Security configuration (CORS, password encoding)

## API Endpoints
### User
- `POST /api/users/register` — Register a new user
- `POST /api/users/login` — Login with email and password

### Credit Cards
- `GET /api/cards` — Get all credit cards
- `POST /api/cards` — Add a new credit card

### Misc
- `GET /api/message` — Test endpoint (returns greeting)

## Security
- Passwords are hashed using BCrypt before storage.
- CORS is enabled for frontend development (`http://localhost:5173`).
- Sensitive endpoints require proper validation.

## Modifying the Application
- **Models**: Add new models in `model/` and annotate with `@Document`.
- **Controllers**: Add new REST endpoints in `controller/`.
- **Repositories**: Extend `MongoRepository` for new data access layers.
- **Config**: Update `config/SecurityConfig.java` for security changes.

---

For more details, see the code and comments in each directory.
