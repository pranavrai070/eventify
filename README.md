
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
