# Node.js Express App with Authentication and User CRUD (MySQL)

This project is a Node.js application built with Express.js, featuring user authentication and CRUD operations using MySQL. It includes middleware for authentication, separate routers, controllers, and models, and unit tests using Jest.

## Features

- User authentication (register and login)
- User CRUD operations
- JWT-based authentication middleware
- MySQL integration using Sequelize ORM
- Environment variable management
- Unit tests with Jest

## Project Structure

```
.
├── src/
│   ├── config/
│   │   └── database.js
│   ├── controllers/
│   │   ├── authController.js
│   │   └── userController.js
│   ├── middleware/
│   │   └── auth.js
│   ├── models/
│   │   └── User.js
│   ├── routes/
│   │   ├── auth.js
│   │   └── user.js
│   └── index.js
├── tests/
│   ├── auth.test.js
│   └── user.test.js
├── .env
├── .gitignore
├── package.json
└── README.md
```

## Getting Started

1. Clone the repository
2. Install dependencies: `npm install`
3. Set up your MySQL database
4. Create a `.env` file with the following variables:
   ```
   PORT=3000
   DB_HOST=your_mysql_host
   DB_USER=your_mysql_user
   DB_PASSWORD=your_mysql_password
   DB_NAME=your_database_name
   JWT_SECRET=your_jwt_secret
   ```
5. Run the application: `npm start`
6. For development with auto-restart: `npm run dev`

## Running Tests

To run the unit tests: `npm test`

## API Endpoints

- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login and receive a JWT token
- GET /api/users - Get all users (requires authentication)
- GET /api/users/:id - Get a specific user (requires authentication)
- PUT /api/users/:id - Update a user (requires authentication)
- DELETE /api/users/:id - Delete a user (requires authentication)

## Contributing

Please feel free to submit issues, fork the repository and send pull requests!

## License

This project is licensed under the MIT License.