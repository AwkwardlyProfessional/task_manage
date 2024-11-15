# Task Management Application

## Overview

The Task Management Application is a web-based tool designed to help users schedule, manage, and prioritize their tasks efficiently. Users can create, edit, delete, and view tasks with different levels of priority and completion status. The app also includes features for sending email reminders about upcoming tasks, managing user accounts, and allowing users to set up email alerts.

## Features

- **User Authentication:** Users can sign up, log in, and log out. Passwords are securely stored using hashing.
- **Task Management:** Users can create, edit, delete, and view tasks. Each task has a name, date, time, duration, notes, and priority level.
- **Email Alerts:** Users can set email alerts to receive notifications for upcoming tasks or completed tasks.
- **Task Prioritization:** Tasks can be prioritized to help users focus on high-priority items.
- **Password Reset:** Users can reset their passwords if they forget them by receiving a password reset email.

## Tech Stack

- **Backend:** Python with Flask
- **Database:** PostgreSQL (or SQLite as fallback)
- **Authentication:** Flask-Login
- **Email:** Flask-Mail for sending email alerts
- **Form Handling:** Flask-WTF
- **Styling:** HTML, CSS (Bootstrap for responsiveness)
- **Version Control:** Git (GitHub)

## Setup Instructions

### Prerequisites

Before setting up the project, make sure you have the following installed:

- **Python 3.x**: Download it from [python.org](https://www.python.org/downloads/).
- **PostgreSQL**: You can use PostgreSQL for production, or use SQLite for local development. If using PostgreSQL, make sure the connection URL is set properly in the environment variables.

### 1. Clone the Repository

First, clone the repository to your local machine:
git clone https://github.com/YourGitHubUsername/Task-Management-App.git
cd Task-Management-App
2. Install Dependencies
Create a virtual environment and activate it:

bash
Copy code
python3 -m venv venv
source venv/bin/activate   # On Windows, use venv\Scripts\activate
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
3. Set Environment Variables
Set the following environment variables for configuration:

SECRET_KEY: Used for session management (you can use secrets.token_hex(24) to generate one).
MAIL_USERNAME: Your email address (used to send emails).
MAIL_PASSWORD: Your email password or app-specific password (if using Gmail).
DATABASE_URL: Your PostgreSQL connection URL (for example, postgres://user:password@localhost/dbname). If you're using SQLite, use sqlite:///default.db.
You can set these variables in your terminal or create a .env file and use a library like python-dotenv to load them automatically.

4. Initialize the Database
Run the following commands to create the database and tables:

bash
Copy code
flask db upgrade
This will create the necessary tables for users and tasks in the database.

5. Run the Application
To start the development server, run:

bash
Copy code
flask run
Your application will be available at http://localhost:5000.

Usage
Sign Up: Create an account by providing a username, email, and password.
Log In: Use your credentials to log in to the application.
Create Tasks: Use the dashboard to add new tasks with details such as name, date, time, duration, and priority.
Set Email Alerts: Configure email alerts for task reminders and updates.
Task Management: View, edit, and delete your tasks as needed.
Additional Information
Password Hashing
The application uses Werkzeug's generate_password_hash function to securely hash passwords before storing them in the database. This ensures that user credentials are never stored in plain text.

Email Alerts
Email alerts are sent using Flask-Mail. You can configure SMTP settings in the MAIL_SERVER, MAIL_PORT, MAIL_USERNAME, and MAIL_PASSWORD environment variables.

Database
The application uses SQLAlchemy for database management, and supports both PostgreSQL and SQLite databases. The default setup is for SQLite, but PostgreSQL can be configured by setting the DATABASE_URL environment variable.

File Structure
plaintext
Copy code
/Task-Management-App
├── app.py                # Main application file
├── models.py             # Database models
├── forms.py              # Forms for user input
├── templates/            # HTML templates
├── static/               # Static files (CSS, JS)
├── requirements.txt      # Project dependencies
├── .env                  # Environment variables (optional)
└── README.md             # Project documentation
Troubleshooting
Missing environment variables: Ensure that all required environment variables are set, including database URL and email credentials.
Database Issues: If using PostgreSQL, make sure the database exists and is accessible. Check the connection URL for correctness.
Email not sending: Double-check your email credentials and SMTP server settings.
License
This project is licensed under the MIT License.

Contact
For any questions or contributions, feel free to reach out to me at [YourEmail@example.com] or submit a pull request!
