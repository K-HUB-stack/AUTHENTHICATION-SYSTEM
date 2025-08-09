# AUTHENTHICATION-SYSTEM
An authentication system is a security mechanism used to verify the identity of users or systems before granting access to resources such as applications networks and even databases.
 Flask Authentication System

A comprehensive authentication system built with Flask, featuring user registration, login, logout, and secure password handling.

Features

- ✅ User Registration with validation
- ✅ User Login with "Remember Me" functionality
- ✅ Secure password hashing using bcrypt
- ✅ Session management with Flask-Login
- ✅ Protected routes requiring authentication
- ✅ Modern, responsive UI with Bootstrap 5
- ✅ Form validation with WTForms
- ✅ SQLAlchemy database integration
- ✅ Flash messaging system
- ✅ User dashboard and profile pages

 Installation

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Set up environment variables:
   - Copy `.env` file and update the `SECRET_KEY` for production use
   - Optionally change the `DATABASE_URL` if you want to use a different database

3. Run the application:
   ```bash
   python app.py
   ```

4. Access the application:
   - Open your browser and go to `http://localhost:5000`

 Project Structure
AUTH/
├── app.py              # Main Flask application
├── requirements.txt    # Python dependencies
├── .env               # Environment variables
├── README.md          # This file
├── auth.db            # SQLite database (created automatically)
└── templates/         # HTML templates
    ├── base.html      # Base template with navigation
    ├── home.html      # Landing page
    ├── register.html  # User registration form
    ├── login.html     # User login form
    ├── dashboard.html # User dashboard (protected)
    └── profile.html   # User profile page (protected)
Usage
Registration
1. Navigate to `/register`
2. Fill in username, email, and password
3. Password must be at least 6 characters
4. Username and email must be unique
Login
1. Navigate to `/login`
2. Enter your email and password
3. Optionally check "Remember Me" for persistent login
4. Access protected dashboard and profile pages
Security Features
- Passwords are hashed using bcrypt
- CSRF protection with Flask-WTF
- Session-based authentication
- Protected routes require login
API Endpoints
- `GET /` - Home page
- `GET/POST /register` - User registration
- `GET/POST /login` - User login
- `GET /logout` - User logout
- `GET /dashboard` - User dashboard (protected)
- `GET /profile` - User profile (protected)

Database Schema
User Model
- `id` (Integer, Primary Key)
- `username` (String, Unique, Required)
- `email` (String, Unique, Required)
- `password_hash` (String, Required)
- `date_created` (DateTime, Default: UTC Now)
- `is_active` (Boolean, Default: True)
 Technologies Used
- Flask - Web framework
- Flask-SQLAlchemy - Database ORM
- Flask-Bcrypt - Password hashing
- Flask-Login - Session management
- Flask-WTF - Form handling and CSRF protection
- WTForms - Form validation
- Bootstrap 5 - Frontend styling
- Font Awesome - Icons
- SQLite - Database (default)
Security Considerations
1. Change the SECRET_KEY in production
2. Use HTTPS  in production
3. Consider rate limiting  for login attempts
4. Regular security updates   for dependencies
5. Database backups   for production use

 Future Enhancements
- Password reset functionality
- Email verification
- Two-factor authentication
- Admin panel
- User role management
- API endpoints with JWT tokens


