<h1 align="center">Frontend – Credit Card Recommender</h1>

<p align="center">
  <img src="../frontend/public/vite.svg" alt="Frontend Logo" width="100" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-18-blue?logo=react" />
  <img src="https://img.shields.io/badge/TypeScript-4.x-blue?logo=typescript" />
  <img src="https://img.shields.io/badge/Vite-fast-646cff?logo=vite" />
  <img src="https://img.shields.io/badge/CSS%20Modules-styles-green" />
</p>

---

## 🌟 Overview
This is the frontend for the Credit Card Recommender app. It provides a modern, responsive UI for users to register, log in, and receive personalized credit card recommendations.

---

## 🖼️ UI Preview
> _Add your own screenshots here!_

<p align="center">
  <img src="https://placehold.co/600x300?text=Dashboard+UI" alt="Dashboard UI"/>
  <img src="https://placehold.co/300x500?text=Mobile+View" alt="Mobile UI"/>
</p>

---

## 📦 Structure
```
frontend/
  src/
    components/
      auth/           # LoginForm, SignupForm
      CreditCardWidget.tsx
    pages/            # Dashboard, LoginPage, SignupPage
    styles/           # CSS modules
    assets/
  public/
    vite.svg          # Logo
  index.html
```

---

## 🔄 Workflow

```mermaid
graph LR
    U["User"] -- Registers/Logs in --> F["Frontend (React)"]
    F -- Sends API request --> B["Backend (Spring Boot)"]
    B -- Reads/Writes --> D["MongoDB"]
    B -- Sends response --> F
    F -- Shows recommendations --> U
```

---

## ✨ Main Components & Pages
- **LoginPage / SignupPage**: Entry points for authentication
- **Dashboard**: Search/filter credit cards by income, credit score, preferences
- **CreditCardWidget**: Visual card display
- **LoginForm / SignupForm**: Handles user authentication

---

## ⚡ Quickstart
```bash
cd frontend
npm install
npm run dev
```
App runs at [http://localhost:5173](http://localhost:5173)

---

## 🔗 API Integration
- Communicates with backend at `http://localhost:8080`
- Endpoints:
  - `POST /api/users/login` — User login
  - `POST /api/users/register` — User registration
  - `GET /api/cards` — Fetch credit card data

---

## 🛠️ Development Tips
- Update API URLs if backend runs on a different port
- Use React DevTools for debugging
- Build for production: `npm run build`

---

## 📄 License
[MIT](../LICENSE)
