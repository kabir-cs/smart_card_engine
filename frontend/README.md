# Frontend

This is the frontend for the Credit Card Recommender application. It is built with React, TypeScript, and Vite for a fast, modern user experience.

---

## Table of Contents
- [Overview](#overview)
- [Setup](#setup)
- [Project Structure](#project-structure)
- [Main Components & Pages](#main-components--pages)
- [Styling](#styling)
- [API Integration](#api-integration)
- [Development Tips](#development-tips)

---

## Overview
The frontend provides a responsive UI for users to register, log in, and receive personalized credit card recommendations based on their profile. It communicates with the backend via REST APIs.

## Setup
1. Ensure you have **Node.js** (v16+ recommended) and **npm** installed.
2. Navigate to the `frontend` directory.
3. Install dependencies:
   ```bash
   npm install
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```
5. The app will be available at [http://localhost:5173](http://localhost:5173)

## Project Structure
- `src/components/` — Reusable UI components
  - `auth/` — Authentication forms (`LoginForm`, `SignupForm`)
  - `CreditCardWidget.tsx` — Displays credit card details
- `src/pages/` — Main pages (`Dashboard`, `LoginPage`, `SignupPage`)
- `src/styles/` — CSS modules for styling
- `public/` — Static assets

## Main Components & Pages
- **LoginPage / SignupPage**: Entry points for authentication, wrapping `LoginForm` and `SignupForm`.
- **Dashboard**: Main page for searching and filtering credit cards by income, credit score, and preferences.
- **CreditCardWidget**: Displays detailed information about a credit card.
- **LoginForm / SignupForm**: Handle user authentication and registration, communicating with backend endpoints.

## Styling
- All styles are located in `src/styles/` and component-specific CSS files.
- The UI is responsive and works well on both desktop and mobile.

## API Integration
- The frontend communicates with the backend at `http://localhost:8080` (default).
- Endpoints used:
  - `POST /api/users/login` — User login
  - `POST /api/users/register` — User registration
  - `GET /api/cards` — Fetch credit card data

## Development Tips
- Update API URLs in components if your backend runs on a different port.
- Use React DevTools and browser console for debugging.
- For production, build the app with `npm run build` and serve the static files.

---

For more details, see the code and comments in each component and page.
