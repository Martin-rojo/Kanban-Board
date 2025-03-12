# Secure Kanban Board

A full-stack Kanban board application with JWT authentication for secure task management.

## Description

The Secure Kanban Board is a web application designed for agile teams to manage their work tasks securely. It features a drag-and-drop interface for organizing tasks across different workflow stages (To Do, In Progress, Done) and implements JWT authentication to ensure that only authorized users can access their boards.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Secure Authentication**
  - JWT-based authentication system
  - Protected routes requiring authentication

- **Kanban Board Functionality**
  - Create, read, update, and delete tasks
  - Drag-and-drop interface for moving tasks between columns
  - Task categorization (To Do, In Progress, Done)
  - Task edit and delete capabilities

- **User Experience**
  - Responsive design for various screen sizes
  - Clean, neutral color palette with good contrast
  - Intuitive navigation and feedback

## Technologies Used

### Frontend
- React.js
- TypeScript
- Fetch API for HTTP requests
- Local storage for JWT persistence

### Backend
- Node.js
- Express.js
- TypeScript
- JSON Web Tokens (JWT) for authentication
- MongoDB for data storage
- Mongoose ODM

### Deployment
- Render for hosting both client and server applications

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/secure-kanban-board.git
   cd secure-kanban-board
   ```

2. Install dependencies for both client and server:
   ```bash
   # Install server dependencies
   cd server
   npm install

   # Install client dependencies
   cd ../client
   npm install
   ```

3. Create a `.env` file in the server directory with the following variables:
   ```
   PORT=3001
   DB_USERNAME=your_database_username
   DB_PASSWORD=your_database_password
   JWT_SECRET=your_jwt_secret_key
   JWT_EXPIRATION=1h
   MONGODB_URI=your_mongodb_connection_string
   ```

## Usage

1. Start the server:
   ```bash
   cd server
   npm start
   ```

2. In a separate terminal, start the client:
   ```bash
   cd client
   npm start
   ```

3. Access the application at `http://localhost:3000`

4. Log in with your credentials or use the default test account:
   - Username: `testuser`
   - Password: `password123`

## API Documentation

### Authentication Endpoints

- `POST /api/auth/login`
  - Request body: `{ username, password }`
  - Response: `{ token, user }`

- `POST /api/auth/logout`
  - Protected route
  - Invalidates the current JWT

### Task Endpoints

- `GET /api/tickets`
  - Protected route
  - Retrieves all tickets for the authenticated user

- `POST /api/tickets`
  - Protected route
  - Creates a new ticket
  - Request body: `{ title, description, status }`

- `PUT /api/tickets/:id`
  - Protected route
  - Updates an existing ticket
  - Request body: `{ title, description, status }`

- `DELETE /api/tickets/:id`
  - Protected route
  - Deletes a ticket

## Screenshots

<img width="1435" alt="image" src="https://github.com/user-attachments/assets/5221fe9b-5933-4c24-b0db-37f65136b853" />


## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes 
4. Push to the branch 
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Questions and concerns

contact: Martin.rojo101@gmail.com

Github: https://github.com/Martin-rojo

Deployed link: https://kanban-board-6lr1.onrender.com/login
