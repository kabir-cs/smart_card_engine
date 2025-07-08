# Credit Card Recommender

A full-stack web application that helps users find the best credit card recommendations based on their income and credit score. Built with a React + TypeScript + Vite frontend and a Spring Boot + MongoDB backend.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview
This application allows users to:
- Register and log in securely
- Input their income and credit score
- Receive personalized credit card recommendations

The backend is built with Spring Boot and MongoDB, handling authentication, user management, and card data. The frontend is built with React, TypeScript, and Vite, providing a modern, responsive UI.

## Features
- User authentication (registration & login)
- Secure password storage (BCrypt)
- Credit card data filtering based on user profile
- Responsive dashboard with search and filter options
- Clean, modular codebase

## Project Structure
```
Hackathon/
  backend/    # Spring Boot backend (API, DB, auth)
  frontend/   # React + TypeScript + Vite frontend (UI)
```

## Getting Started

### Backend Setup
See [backend/README.md](backend/README.md) for full details.
1. Install Java 17 and Maven.
2. Navigate to `backend/`.
3. Run: `./mvnw spring-boot:run`

### Frontend Setup
See [frontend/README.md](frontend/README.md) for full details.
1. Install Node.js (v16+ recommended).
2. Navigate to `frontend/`.
3. Run: `npm install && npm run dev`

## Usage
- Visit the frontend (default: http://localhost:5173)
- Register or log in
- Use the dashboard to search for credit cards by income, credit score, and preferences

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](LICENSE)
