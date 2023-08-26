# management-login

# Flask Registration System with Document Verification

This application provides a registration system where users sign up in two steps and verify their identity using a provided document. It uses Flask for the web framework, MongoDB as a database, and Flask-Mail to send verification emails.

## Features:

- Two-step signup process.
- Email and document verification.
- U-DISE code validation.
- Secure password hashing.
- User dashboard access post verification.

## Installation

1. **Dependencies**: You need to have Python and pip installed.

2. Clone this repository:

   ```bash
   git clone <repository-url>
Navigate to the project directory:

bash
Copy code
cd <directory-name>
Install required libraries:

bash
Copy code
pip install Flask Flask-Mail Flask-PyMongo python-dotenv werkzeug
Create a .env file in the root directory and add the following variables:

env
Copy code
MAIL_SERVER=your_mail_server
MAIL_PORT=your_mail_port
MAIL_USERNAME=your_mail_username
MAIL_PASSWORD=your_mail_password
MONGO_URI=your_mongo_uri
Usage
Start the Flask application:

bash
Copy code
python <script-name>.py
Navigate to the provided server URL (usually http://127.0.0.1:5000/) in your web browser.

Follow the two-step signup process:

Step 1: Enter username, email, password, mobile number, and submit.
Step 2: Enter institute details and upload a verification document.
Verify your email and document as prompted.

Access the user dashboard post verification.

API Endpoints:
/signup-step1 (POST): Signup Step 1.
/verify-code (POST): Verify email code.
/signup-step2 (POST): Signup Step 2, with document upload.
/get-unverified-documents (GET): Retrieve all unverified documents.
/verify-document (POST): Verify user's document.
/verify-code (POST): Verify the document verification code.
/login (POST): User login.
/dashboard (GET): User dashboard.
Notes:
Ensure you have the proper configurations for Flask-Mail.
The document's path to save needs to be defined.
The application does not handle advanced authentication mechanisms like JWT or session management.
