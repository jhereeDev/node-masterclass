# DevCamper API

A robust RESTful API for managing bootcamp courses and reviews, built with Node.js, Express, and MongoDB.

## Features

- User authentication and authorization
- Bootcamp management (CRUD operations)
- Course management for bootcamps
- Review system
- Advanced filtering, sorting, and pagination
- Security features (XSS protection, rate limiting, etc.)
- File upload functionality
- Email notifications

## Tech Stack

- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- Various security middleware (helmet, xss-clean, etc.)

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd devcamper_api
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory with the following variables:
```
NODE_ENV=development
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
JWT_EXPIRE=30d
JWT_COOKIE_EXPIRE=30
SMTP_HOST=smtp.mailtrap.io
SMTP_PORT=2525
SMTP_EMAIL=your_email
SMTP_PASSWORD=your_password
FROM_EMAIL=noreply@devcamper.com
FROM_NAME=DevCamper
```

## Running the Application

### Development Mode
```bash
npm run dev
```

### Production Mode
```bash
npm start
```

## API Documentation

### Authentication Endpoints
- POST /api/v1/auth/register - Register a new user
- POST /api/v1/auth/login - Login user
- GET /api/v1/auth/me - Get current user
- PUT /api/v1/auth/updatedetails - Update user details
- PUT /api/v1/auth/updatepassword - Update password
- POST /api/v1/auth/forgotpassword - Forgot password
- PUT /api/v1/auth/resetpassword/:resettoken - Reset password

### Bootcamp Endpoints
- GET /api/v1/bootcamps - Get all bootcamps
- GET /api/v1/bootcamps/:id - Get single bootcamp
- POST /api/v1/bootcamps - Create new bootcamp
- PUT /api/v1/bootcamps/:id - Update bootcamp
- DELETE /api/v1/bootcamps/:id - Delete bootcamp

### Course Endpoints
- GET /api/v1/courses - Get all courses
- GET /api/v1/courses/:id - Get single course
- POST /api/v1/bootcamps/:bootcampId/courses - Add course to bootcamp
- PUT /api/v1/courses/:id - Update course
- DELETE /api/v1/courses/:id - Delete course

### Review Endpoints
- GET /api/v1/reviews - Get all reviews
- GET /api/v1/reviews/:id - Get single review
- POST /api/v1/bootcamps/:bootcampId/reviews - Add review to bootcamp
- PUT /api/v1/reviews/:id - Update review
- DELETE /api/v1/reviews/:id - Delete review

## Security Features

- XSS Protection
- SQL Injection Protection
- Rate Limiting
- Security Headers
- CORS Enabled
- Cookie Parser
- MongoDB Sanitization

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.

## Author

Jm Figueroa

