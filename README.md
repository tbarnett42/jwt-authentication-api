# REST API with JWT Authentication

A Node.js/Express REST API implementing user authentication with JWT tokens, password hashing, and MongoDB integration.

## 🎯 Project Overview

This project was built as a learning exercise to understand authentication systems, RESTful API design, and backend development fundamentals. It demonstrates implementation of user registration, login, password security, and token-based authentication.

## 🛠️ Technologies Used

- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **TypeScript** - Type-safe JavaScript
- **MongoDB Atlas** - Cloud database
- **Mongoose** - MongoDB object modeling
- **bcrypt** - Password hashing
- **jsonwebtoken (JWT)** - Token-based authentication
- **cookie-parser** - Cookie handling
- **body-parser** - Request body parsing
- **Postman** - API testing

## 📁 Project Structure

```
A REST API/
├── src/
│   ├── controllers/
│   │   └── authentication.ts    # Login & register logic
│   ├── db/
│   │   └── users.ts             # User model & database operations
│   ├── helpers/
│   │   └── index.ts             # Authentication helpers (hashing, JWT)
│   ├── router/
│   │   ├── authentication.ts    # Auth routes
│   │   └── index.ts             # Main router
│   └── index.ts                 # Server entry point
├── package.json
└── tsconfig.json
```

## 🚀 Features Implemented

✅ User registration with password hashing (bcrypt)
✅ User login with credential verification
✅ JWT token generation
✅ Session token management
✅ MongoDB Atlas integration
✅ RESTful API structure
✅ TypeScript configuration
✅ Express middleware setup

## 📝 API Endpoints

### Authentication

**Register User**
```http
POST /auth/register
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "password123",
  "username": "username"
}
```

**Login User**
```http
POST /auth/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "password123"
}
```

## 🔧 Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- MongoDB Atlas account
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd "A REST API"
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure MongoDB**
   - Update the MongoDB connection string in `src/index.ts`
   - Replace with your own MongoDB Atlas credentials

4. **Update the secret key**
   - In `src/helpers/index.ts`, change the SECRET constant to your own secret

5. **Start the server**
   ```bash
   npm start
   ```

The server will run on `http://localhost:8080` (or the port specified in your config)

## 📚 What I Learned

Through this project, I gained hands-on experience with:

- **RESTful API Design** - Understanding HTTP methods, status codes, and API structure
- **Authentication Systems** - Implementing secure login/registration flows
- **Password Security** - Using bcrypt for hashing and salting passwords
- **JWT Tokens** - Token-based authentication and session management
- **MongoDB** - NoSQL database design and Mongoose ODM
- **TypeScript** - Type safety in Node.js applications
- **Express Middleware** - Request/response handling and middleware chain
- **Debugging** - Troubleshooting routing issues, port conflicts, and server errors
- **API Testing** - Using Postman to test endpoints

## 🐛 Known Issues

- **Routing Configuration**: The authentication routes have connection issues that require further debugging. The routing chain between `index.ts` → `router/index.ts` → `router/authentication.ts` needs to be verified.
- **Export/Import Pattern**: The authentication router uses a function export pattern that may need refactoring for proper route registration.

## 🔮 Future Enhancements

If continuing this project, potential improvements include:

- [ ] Fix routing issues to get login/register fully functional
- [ ] Add middleware for protected routes
- [ ] Implement user profile endpoints
- [ ] Add input validation and sanitization
- [ ] Create comprehensive error handling
- [ ] Add refresh token functionality
- [ ] Implement password reset flow
- [ ] Add rate limiting for security
- [ ] Write unit and integration tests
- [ ] Add API documentation (Swagger/OpenAPI)

## 📖 Tutorial Reference

This project was built following a REST API authentication tutorial, covering:
- Environment setup
- Express server configuration
- MongoDB setup and user models
- Authentication helper functions
- Authentication controllers
- Routing and middleware (in progress)

## 🙏 Acknowledgments

This project represents 3 days of hands-on learning in backend development, debugging, and problem-solving. While not fully complete, it demonstrates foundational understanding of:
- Building REST APIs with Express
- Implementing authentication systems
- Working with databases
- TypeScript in Node.js projects

## 📄 License

This is a personal learning project and is available for educational purposes.

---

**Note**: This project is a work-in-progress learning exercise. The authentication routes require additional debugging before full functionality is achieved.
