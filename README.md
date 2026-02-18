# Flask Authentication App

A simple Flask-based user authentication system with registration, login, and session management.

## Features

- **User Registration**: Create new user accounts with validation
- **User Login**: Secure login with bcrypt password hashing
- **Session Management**: Persistent user sessions
- **Dashboard**: Protected user dashboard accessible only after login
- **Logout**: Clear session and logout functionality

## Validation Rules

- **Name**: Must not be empty
- **Email**: Must not be empty and must be unique
- **Password**: 
  - Must not be empty
  - Must be at least 6 characters long

## Technologies Used

- **Flask**: Web framework
- **SQLAlchemy**: Database ORM
- **SQLite**: Database
- **bcrypt**: Password hashing
- **Bootstrap**: Frontend styling

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

```bash
python app.py
```

The application will run on `http://127.0.0.1:5000/` in debug mode.

## Project Structure

```
Flask_Auth_App/
├── app.py                 # Main application file
├── requirements.txt       # Python dependencies
├── instance/
│   └── database.db       # SQLite database (auto-generated)
└── templates/
    ├── base.html         # Base template
    ├── Index.html        # Home page
    ├── Register.html     # Registration form
    ├── login.html        # Login form
    └── dashboard.html    # User dashboard
```

## Routes

- `/` - Home page
- `/register` - User registration
- `/login` - User login
- `/dashboard` - Protected user dashboard (login required)
- `/logout` - Logout and clear session