# Task Manager

A full-stack task management application built with Node.js, Express, and MongoDB for the backend, and React, Vite, and Redux for the frontend. It allows users to create, manage, and track tasks with features like user authentication, role-based access, attachments, todo checklists, and progress tracking.

## Features

- **User Authentication & Authorization**: Secure login/signup with JWT tokens and role-based access (Admin and User roles).
- **Task Management**: Create, edit, assign, and track tasks with priorities, statuses, due dates, and progress.
- **Todo Checklists**: Add and manage sub-tasks within each task.
- **File Attachments**: Upload and manage attachments for tasks.
- **Dashboard & Reports**: View dashboards with charts, generate reports on tasks.
- **Responsive UI**: Built with Tailwind CSS for a modern, responsive design.
- **Real-time Updates**: Integrated with Redux for state management.

## Tech Stack

### Backend
- **Node.js**: JavaScript runtime for server-side development.
- **Express.js**: Web framework for building APIs.
- **MongoDB**: NoSQL database with Mongoose ODM.
- **JWT**: JSON Web Tokens for authentication.
- **bcryptjs**: Password hashing.
- **multer**: File upload handling.
- **cors & cookie-parser**: Middleware for cross-origin requests and cookies.

### Frontend
- **React**: Library for building user interfaces.
- **Vite**: Fast build tool and development server.
- **Redux Toolkit**: State management.
- **Tailwind CSS**: Utility-first CSS framework.
- **Axios**: HTTP client for API requests.
- **React Router DOM**: Client-side routing.
- **React Hot Toast**: Notifications.
- **Recharts**: Chart library for data visualization.
- **React Datepicker**: Date selection component.

## Prerequisites

- Node.js (version 14 or higher)
- MongoDB (local or cloud instance like MongoDB Atlas)
- npm or yarn package manager

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/task-manager.git
   cd task-manager
   ```

2. **Install backend dependencies**:
   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**:
   ```bash
   cd ../frontend
   npm install
   ```

## Environment Variables

Create a `.env` file in the `backend` directory and add the following variables:

```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
FRONT_END_URL=http://localhost:5173
```

- `MONGO_URI`: Connection string for your MongoDB database.
- `JWT_SECRET`: A secret key for signing JWT tokens.
- `FRONT_END_URL`: URL of the frontend application (default for development).

## Running the Application

1. **Start the backend server**:
   ```bash
   cd backend
   npm run dev
   ```
   The backend server will start on `http://localhost:3000`.

2. **Start the frontend development server**:
   ```bash
   cd frontend
   npm run dev
   ```
   The frontend will be available at `http://localhost:5173`.

3. **Build for production** (optional):
   ```bash
   cd frontend
   npm run build
   npm run preview
   ```

## API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/signin` - User login
- `POST /api/auth/signout` - User logout

### Users
- `GET /api/users` - Get all users (Admin only)
- `PUT /api/users/:id` - Update user details
- `DELETE /api/users/:id` - Delete user (Admin only)

### Tasks
- `GET /api/tasks` - Get all tasks
- `POST /api/tasks` - Create a new task
- `PUT /api/tasks/:id` - Update a task
- `DELETE /api/tasks/:id` - Delete a task

### Reports
- `GET /api/reports/tasks` - Generate task reports

## Project Structure

```
task-manager/
├── backend/
│   ├── controller/          # Route controllers
│   ├── models/              # MongoDB models
│   ├── routes/              # API routes
│   ├── utils/               # Utility functions
│   ├── uploads/             # File uploads directory
│   ├── index.js             # Server entry point
│   └── package.json
├── frontend/
│   ├── public/              # Static assets
│   ├── src/
│   │   ├── components/      # Reusable components
│   │   ├── pages/           # Page components
│   │   ├── redux/           # State management
│   │   ├── routes/          # Routing logic
│   │   └── utils/           # Helper functions
│   ├── index.html
│   └── package.json
└── README.md
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

## License

This project is licensed under the ISC License. See the [LICENSE](LICENSE) file for details.

## Screenshots

*(Add screenshots here if available)*

## Contact

For questions or support, please open an issue on GitHub.
