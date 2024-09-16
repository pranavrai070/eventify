
# Event Management App

## Overview

The **Event Management App** is a full-stack web application that simplifies the process of managing and attending events. Users can view events, register, and keep track of upcoming events, while admins can create, update, and delete events. The app leverages a RESTful API, providing a modern and user-friendly interface for both participants and administrators.

## Features

### User Features
- **Browse Events**: Users can view a list of all upcoming events.
- **Event Details**: Each event comes with detailed information such as the date, location, and description.
- **Event Registration**: Users can register for an event, and view a list of their registered events.
- **Search Functionality**: Search events by category or date.
  
### Admin Features
- **Create Events**: Admins can create new events.
- **Edit Events**: Admins can modify existing events.
- **Delete Events**: Admins can remove events.
- **View Registrants**: Admins can view a list of users registered for an event.

### General Features
- **Authentication**: Secure sign-up and login for users and admins with JSON Web Tokens (JWT).
- **Responsive Design**: Fully responsive UI, designed to work on both mobile and desktop devices.

## Tech Stack

### Frontend
- **React**: A popular JavaScript library for building user interfaces.
- **React Router**: For routing and navigation between pages.
- **Axios**: For making API requests to the backend.
- **CSS**: For styling the application, making it visually appealing and responsive.

### Backend
- **Node.js**: JavaScript runtime for the server-side code.
- **Express**: Minimalist web framework for building the API.
- **JWT**: JSON Web Tokens for secure authentication.
  
### Database
- **MongoDB**: NoSQL database for storing event and user data.
- **Mongoose**: ODM (Object Data Modeling) library for MongoDB, used for schema modeling.

## Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v14 or above)
- **MongoDB** (local instance or [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) for cloud database)

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/event-management-app.git
cd event-management-app
```

### 2. Install Dependencies

#### Backend

Navigate to the `backend` directory and install the necessary packages:

```bash
cd backend
npm install
```

#### Frontend

Navigate to the `frontend` directory and install the necessary packages:

```bash
cd frontend
npm install
```

### 3. Setup Environment Variables

Create a `.env` file in the **backend** directory and set the following environment variables:

```
MONGO_URI=your-mongodb-uri
JWT_SECRET=your-secret-key
PORT=5000
```

- `MONGO_URI`: The connection string for your MongoDB instance.
- `JWT_SECRET`: A secret key used to sign JWT tokens.
- `PORT`: The port number on which your backend server will run.

### 4. Start the Application

#### Backend

Start the backend server by running the following command in the `backend` directory:

```bash
npm start
```

The backend will run on `http://localhost:5000`.

#### Frontend

In a new terminal, start the frontend React app by running the following command in the `frontend` directory:

```bash
npm start
```

The frontend will run on `http://localhost:3000`.

## API Documentation

### Authentication

| Method | Endpoint          | Description          | Access  |
|--------|-------------------|----------------------|---------|
| POST   | `/api/auth/signup` | User sign up         | Public  |
| POST   | `/api/auth/login`  | User login           | Public  |

### Events

| Method | Endpoint                  | Description                      | Access     |
|--------|---------------------------|----------------------------------|------------|
| GET    | `/api/events`              | Get all events                   | Public     |
| POST   | `/api/events`              | Create a new event               | Admin only |
| PUT    | `/api/events/:id`          | Update an event                  | Admin only |
| DELETE | `/api/events/:id`          | Delete an event                  | Admin only |
| GET    | `/api/events/:id`          | Get event details by ID          | Public     |
| POST   | `/api/events/:id/register` | Register a user for the event    | User only  |

### Example API Request

Here’s an example of a request to register a user for an event:

```bash
POST /api/events/:id/register
Authorization: Bearer <JWT Token>
{
  "userId": "user123"
}
```

## Folder Structure

```bash
event-management-app/
│
├── backend/                # Node.js backend (Express)
│   ├── models/             # Mongoose models (Event, User)
│   ├── routes/             # Express routes for API
│   ├── controllers/        # Logic for handling API requests
│   └── server.js           # Main server entry point
│
├── frontend/               # React frontend
│   ├── src/
│   │   ├── components/     # React components (EventCard, Navbar, etc.)
│   │   ├── pages/          # Pages for different routes (Home, EventDetail)
│   │   ├── App.js          # Main React app entry point
│   └── public/             # Public assets (HTML, CSS)
│
└── README.md               # Documentation file
```

## Future Enhancements

Here are some potential future improvements for the app:

- **Event Categories**: Add more filtering options for events by category.
- **Notifications**: Implement a system to notify users about event updates.
- **Payment Integration**: Add support for paid events with integration to payment gateways like Stripe or PayPal.
- **Calendar View**: Introduce a calendar view to visualize upcoming events in a more user-friendly way.

## Contributing

Contributions are welcome! To contribute:

1. Fork the project
2. Create your feature branch (`git checkout -b feature/NewFeature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature/NewFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries or support, please email: [your-email@example.com](mailto:your-email@example.com).
