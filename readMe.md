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

2. Create and activate virtual environment:

```bash
python -m venv env
source env/bin/activate  # For MacOS/Linux
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Create a .env file in the root directory:

```bash
touch .env
```

5. Add the following configuration to your .env file:

```plaintext
# JWT Configuration
SECRET_KEY="your_secret_key_here"
ALGORITHM="HS256"
ACCESS_TOKEN_EXPIRE_MINUTES=30

# Database Configuration
DATABASE_URL="sqlite:///./users.db"
```

6. Run the application:

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
- Environment variables for sensitive data

## Development

To start the development server with hot reload:

```bash
uvicorn main:app --reload --port 8000
```

## Environment Variables

The application requires the following environment variables in the .env file:

- `SECRET_KEY`: JWT secret key for token generation
- `ALGORITHM`: JWT algorithm (default: "HS256")
- `ACCESS_TOKEN_EXPIRE_MINUTES`: Token expiration time in minutes
- `DATABASE_URL`: SQLite database URL

Make sure to keep your .env file secure and never commit it to version control.

## License

[Your chosen license]

## Contributing

[Your contribution guidelines]

```

The updated README now includes:
1. Virtual environment setup instructions
2. .env file creation and configuration
3. Detailed environment variables section
4. Security note about keeping .env file secure









```
