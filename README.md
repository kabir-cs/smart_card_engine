<p align="center">
  <img src="frontend/public/vite.svg" alt="Project Logo" width="120" />
</p>

<h1 align="center">Credit Card Recommender</h1>

<p align="center">
  <b>Find the best credit card for you, instantly.</b><br/>
  <a href="#workflow">Workflow</a> • <a href="#features">Features</a> • <a href="#tech-stack">Tech Stack</a> • <a href="#getting-started">Getting Started</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/frontend-React-blue?logo=react" />
  <img src="https://img.shields.io/badge/backend-SpringBoot-green?logo=spring" />
  <img src="https://img.shields.io/badge/database-MongoDB-brightgreen?logo=mongodb" />
  <img src="https://img.shields.io/badge/build-Vite-646cff?logo=vite" />
  <img src="https://img.shields.io/badge/language-TypeScript-blue?logo=typescript" />
</p>

---

## 🚀 Project Overview
Credit Card Recommender is a full-stack web app that helps users discover the best credit cards based on their income and credit score. It features secure authentication, a modern UI, and real-time recommendations.

---

## 🛠️ Tech Stack
- **Frontend:** React, TypeScript, Vite, CSS Modules
- **Backend:** Spring Boot, Java 17, MongoDB
- **Security:** BCrypt password hashing, CORS

---

## 🔄 Workflow

### System Architecture

```mermaid
flowchart TD
    A["User visits frontend"] --> B["Frontend (React + Vite)"]
    B -->|"API Request"| C["Backend (Spring Boot)"]
    C -->|"Query"| D["MongoDB Database"]
    D -->|"Results"| C
    C -->|"API Response"| B
    B --> E["User sees recommendations"]
    subgraph "Frontend"
      B
    end
    subgraph "Backend"
      C
      D
    end
```

### User Journey

```mermaid
sequenceDiagram
    participant U as "User"
    participant F as "Frontend (React)"
    participant B as "Backend (Spring Boot)"
    participant DB as "MongoDB"
    U->>F: Register/Login
    F->>B: POST /api/users/register or /login
    B->>DB: Store/verify user
    DB-->>B: Success/failure
    B-->>F: Auth result
    U->>F: Search for cards
    F->>B: GET /api/cards
    B->>DB: Query cards
    DB-->>B: Card data
    B-->>F: Card results
    F-->>U: Show recommendations
```

---

## ✨ Features
- User registration & login (secure, hashed passwords)
- Personalized credit card recommendations
- Filter by income, credit score, and preferences
- Responsive dashboard UI
- Modern, maintainable codebase

---

## 📁 Project Structure
```
Hackathon/
  backend/    # Spring Boot backend (API, DB, auth)
  frontend/   # React + TypeScript + Vite frontend (UI)
```

---

## ⚡ Getting Started

### Backend
See [backend/README.md](backend/README.md) for full details.
```bash
cd backend
./mvnw spring-boot:run
```

### Frontend
See [frontend/README.md](frontend/README.md) for full details.
```bash
cd frontend
npm install
npm run dev
```

---

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## 📄 License
[MIT](LICENSE)
