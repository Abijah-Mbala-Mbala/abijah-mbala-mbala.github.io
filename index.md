---
layout: "default"
title: "AuthSystem: Secure Node.js Authentication with JWT and Cloudinary"
description: "Implement a secure authentication system with user registration, login, email verification, and profile management. Explore the code on GitHub! 🚀🌟"
---
# AuthSystem: Secure Node.js Authentication with JWT and Cloudinary

![AuthSystem](https://img.shields.io/badge/AuthSystem-Secure%20Authentication-brightgreen)
![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-yellowgreen)

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Overview

AuthSystem is a secure authentication system built using Node.js. It leverages JSON Web Tokens (JWT) for user authentication and supports email and text verification. With Cloudinary integration, it allows users to upload and manage images efficiently. The system is designed for scalability and safety, using MongoDB as the backend database.

You can download the latest release [here](https://github.com/Abijah-Mbala-Mbala/AuthSystem/releases).

---

## Features

- **JWT Authentication**: Secure user sessions with JSON Web Tokens.
- **Email Verification**: Users must verify their email addresses to enhance security.
- **Text Verification**: An additional layer of verification through SMS.
- **Cloudinary Support**: Upload and manage images seamlessly.
- **MongoDB Backend**: A robust and scalable database solution.
- **RESTful API**: Easy integration with front-end applications.
- **Secure Password Storage**: Passwords are hashed for security.
- **Role-Based Access Control**: Manage user permissions effectively.

---

## Technologies Used

- **Node.js**: JavaScript runtime for building server-side applications.
- **Express.js**: Web framework for Node.js.
- **MongoDB**: NoSQL database for data storage.
- **Mongoose**: ODM for MongoDB and Node.js.
- **jsonwebtoken**: Library for JWT creation and verification.
- **nodemailer**: Module for sending emails.
- **twilio**: Service for sending SMS messages.
- **Cloudinary**: Image management service.
- **dotenv**: Module for managing environment variables.

---

## Installation

To get started with AuthSystem, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Abijah-Mbala-Mbala/AuthSystem.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd AuthSystem
   ```

3. **Install dependencies**:

   ```bash
   npm install
   ```

4. **Set up environment variables**:

   Create a `.env` file in the root directory and add the following variables:

   ```plaintext
   PORT=3000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   EMAIL_SERVICE=your_email_service
   EMAIL_USER=your_email_user
   EMAIL_PASS=your_email_password
   TWILIO_ACCOUNT_SID=your_twilio_account_sid
   TWILIO_AUTH_TOKEN=your_twilio_auth_token
   TWILIO_PHONE_NUMBER=your_twilio_phone_number
   CLOUDINARY_URL=your_cloudinary_url
   ```

5. **Run the application**:

   ```bash
   npm start
   ```

The application should now be running on `http://localhost:3000`.

---

## Usage

Once the application is running, you can interact with the API using tools like Postman or curl. Below are some examples of how to use the API endpoints.

### User Registration

To register a new user, send a POST request to `/api/auth/register` with the following JSON body:

```json
{
  "username": "exampleUser",
  "email": "user@example.com",
  "password": "yourpassword"
}
```

### User Login

To log in, send a POST request to `/api/auth/login` with the following JSON body:

```json
{
  "email": "user@example.com",
  "password": "yourpassword"
}
```

### Email Verification

After registration, users will receive an email with a verification link. Clicking the link will send a GET request to `/api/auth/verify/:token` to verify the email.

### Text Verification

To send a text verification code, call the endpoint `/api/auth/send-verification-code` after logging in. The user will receive a code via SMS.

---

## API Endpoints

Here are the main API endpoints available in AuthSystem:

| Method | Endpoint                        | Description                     |
|--------|---------------------------------|---------------------------------|
| POST   | `/api/auth/register`            | Register a new user            |
| POST   | `/api/auth/login`               | Log in a user                  |
| GET    | `/api/auth/verify/:token`       | Verify user email              |
| POST   | `/api/auth/send-verification-code` | Send SMS verification code    |
| POST   | `/api/auth/verify-code`         | Verify the SMS code            |
| POST   | `/api/upload`                   | Upload an image to Cloudinary  |

---

## Testing

To run tests for the application, use the following command:

```bash
npm test
```

Make sure to have a test database set up in your `.env` file for testing purposes.

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/YourFeature`).
6. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Contact

For any inquiries, please contact:

- **Author**: Abijah Mbala Mbala
- **Email**: abijah@example.com
- **GitHub**: [Abijah-Mbala-Mbala](https://github.com/Abijah-Mbala-Mbala)

You can also download the latest release [here](https://github.com/Abijah-Mbala-Mbala/AuthSystem/releases).

---