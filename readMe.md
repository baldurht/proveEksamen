# Beer Collection Web Application

A secure web application for browsing and sorting beer collections, built with FastAPI and JavaScript.

## Features

- **User Authentication**
  - Secure signup and login system
  - JWT-based authentication
  - Password hashing with bcrypt

- **Beer Collection Display**
  - Grid layout of beer cards
  - Image display with fallback placeholder
  - Responsive design
  - Interactive card hover effects

- **Sorting Functionality**
  - Sort by name (alphabetically)
  - Sort by rating (highest to lowest)
  - Sort by price (lowest to highest)

## Technology Stack

- **Backend**
  - FastAPI (Python web framework)
  - SQLAlchemy (ORM)
  - JWT for authentication
  - bcrypt for password hashing
  - SQLite database

- **Frontend**
  - Vanilla JavaScript
  - HTML5
  - CSS3
  - Responsive design

## Installation

1. Clone the repository:
```bash
git clone https://github.com/baldurht/proveEksamen
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
uvicorn main:app --reload
```

## API Endpoints

- `GET /` - Login page
- `GET /signup` - Signup page
- `POST /signup` - Create new user
- `POST /login` - Authenticate user
- `GET /main` - Main application page
- `GET /get-beers` - Fetch beer collection (protected route)

## Database Schema

### Users Table
- id (Integer, Primary Key)
- username (String, Unique)
- hashed_password (String)

## Security Features

- Password hashing using bcrypt
- JWT token-based authentication
- HTTP-only cookies for token storage
- Protected API endpoints
- Input validation and sanitization

## Development

To start the development server with hot reload:

```bash
uvicorn main:app --reload --port 8000
```
