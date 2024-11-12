Secure Authentication System
============================

This project demonstrates a secure Level 3 authentication system using:
- **OAuth (Google Strategy)** for third-party authentication.
- **Local Authentication** with password security enhancements using salting and bcrypt hashing.
- **Database Security** best practices for securely storing sensitive information.

This guide includes setup instructions for Google OAuth, configuring the session secret, and setting up the PostgreSQL database.

Project Features:
-----------------
1. **Google OAuth Strategy**: Allows users to log in with Google credentials.
2. **Local Authentication**: Users can register and log in with a username and password, which are securely hashed and salted.
3. **Enhanced Password Security**: Uses bcrypt to hash passwords with salting.
4. **Database Security**: Sensitive information is stored securely in PostgreSQL. See `database.png` for the schema details.

## Prerequisites
- Node.js and npm installed.
- PostgreSQL installed and running.
- Google Cloud account to set up the Google OAuth client ID and secret.

## Project Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/abdul-haseeb-code/secure-auth-system.git
   cd secure-auth-system


2 Install Dependencies
npm install


3 Configure Environment Variables In the project directory, create a .env file with the following variables. Replace placeholders with your actual credentials.

4 Setting Up Google OAuth Strategy

Go to Google Cloud Console.
Create a new project (or select an existing one).
Navigate to APIs & Services > Credentials.
Click Create Credentials > OAuth Client ID.
Set the application type to Web application.
Configure authorized redirect URIs (e.g., http://localhost:3000/auth/google/callback).
Copy the Client ID and Client Secret to your .env file.

5 Database Configuration

This project uses PostgreSQL as the database.

The database schema is displayed in database.png. Ensure your PostgreSQL instance reflects this structure.

Connect your PostgreSQL database by setting the DATABASE_URL in .env. Example format:

6 Run Database Migrations
Run the necessary migrations to set up the database tables as per the schema in database.png.
Run the Application

7 Run the Application 
npm start
Your application should now be running on http://localhost:3000.

Security Features
Password Hashing: Uses bcrypt to hash passwords with salting for added security.
OAuth Authentication: Ensures secure authentication using Google as a trusted third-party provider.
Session Management: Uses sessions to keep users authenticated, with a SESSION_SECRET that you should replace in .env with your own unique value.
Usage
Register an Account: For local authentication, register by creating a username and password.
Log In: Log in with either the local strategy (username/password) or Google OAuth.
Database Security: Passwords and sensitive user data are stored securely in PostgreSQL. View database.png for the database schema.
Additional Notes
Environment Configuration: Replace any placeholder values in .env with your own credentials.
OAuth URIs: Ensure redirect URIs in Google Cloud match your local setup.


License
This project is licensed under the MIT License.


This README includes PostgreSQL-specific instructions for setting up and connecting the database. Be sure to customize any placeholders with your actual database and Google Cloud details.





