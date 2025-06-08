# Django React App

This repository contains a simple full-stack notes application with a Django REST API backend and a React frontend built with Vite.

## Project Structure

```
backend/   # Django project
frontend/  # React application
```

### Backend

The backend uses Django and Django REST framework with JWT authentication provided by `djangorestframework-simplejwt`.

Main features:
- User registration and JWT based login.
- CRUD API for personal notes.

### Frontend

The frontend is a single page application created with React and Vite. It includes pages for logging in, registering, and managing notes.

## Getting Started

### Prerequisites
- Python 3.11+
- Node.js 18+
- PostgreSQL database

### Backend Setup

1. Install Python dependencies:
   ```bash
   pip install -r backend/requirements.txt
   ```
2. Configure environment variables for the database in a `.env` file or your shell:
   - `DB_NAME`
   - `DB_USER`
   - `DB_PWD`
   - `DB_HOST`
   - `DB_PORT`
3. Apply migrations and start the server:
   ```bash
   cd backend
   python manage.py migrate
   python manage.py runserver
   ```
   The API will be available at `http://localhost:8000/`.

### Frontend Setup

1. Install dependencies:
   ```bash
   cd frontend
   npm install
   ```
2. (Optional) Define `VITE_API_URL` in a `.env` file to override the API base URL.
3. Start the development server:
   ```bash
   npm run dev
   ```
   The app will run on `http://localhost:5173/` by default.

## Usage

- Visit the frontend URL and register a new user.
- Log in to obtain JWT tokens stored in local storage.
- Create, list, and delete your own notes from the home page.

## License

This project is provided as-is without a specific license.

