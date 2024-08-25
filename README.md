# EventSphere

## Overview

**EventSphere** is a web application designed to streamline the process of event planning and management. Whether you're organizing a small gathering, a large conference, or anything in between, EventSphere offers a comprehensive suite of tools to make event management effortless. The platform is designed for both event organizers and attendees, providing a one-stop solution for all event-related activities.

## Features

### For Organizers:
- **Event Creation**: Easily create events by specifying details such as name, location, date, and an event image.
- **Event Management**: Update or delete your events as needed, and manage RSVPs from attendees.
- **Promotion**: Share your event details and reach a wider audience through integrated promotion tools.
- **Communication**: Automatically send emails to attendees, or manually reach out to them for special updates.

### For Attendees:
- **Event Discovery**: Browse through a variety of events, filter by your interests, and find events that suit your needs.
- **RSVP**: Register for events with a simple click, and manage your RSVPs directly from your profile.
- **Reviews**: Leave reviews and rate events you’ve attended, helping future attendees make informed decisions.
- **Notifications**: Stay up-to-date with the latest event updates and receive reminders for upcoming events.

## Technology Stack

EventSphere is built using the **MERN** stack, a popular set of technologies for full-stack JavaScript development:

- **MongoDB**: A NoSQL database that stores all event and user-related data in a flexible, document-oriented structure.
- **Express.js**: A web application framework for Node.js, used to create robust and scalable server-side APIs.
- **React**: A JavaScript library for building dynamic and responsive user interfaces. The frontend of EventSphere is built with React, utilizing modern development practices such as functional components and hooks.
- **Node.js**: A JavaScript runtime that powers the backend, handling requests, and integrating with the database.

### State Management
- **Context API**: Used in the React frontend to manage global state efficiently. The Context API simplifies state management across the application, allowing different components to access and modify shared data without prop drilling.

### Backend API
- **RESTful API**: The backend is built with Express.js and follows RESTful principles to handle HTTP requests. The API provides endpoints for event management, user authentication, and more.

### Testing
- **Selenium**: Used for testing the frontend GUI, ensuring all components and features work as expected.
- **Jest**: A JavaScript testing framework used to test the Node.js backend. It helps in validating the REST endpoints and ensuring they perform correctly under various conditions.
- **Postman**: A tool used to manually test API endpoints during development. It helps simulate different HTTP requests to ensure that the backend is functioning as intended.
- **Google Lighthouse**: An auditing tool used to evaluate the performance, accessibility, SEO, and best practices of the web application.

## Architecture

### Client-Server Architecture
EventSphere follows a **client-server architecture**, with a clear division of responsibilities:

- **Client**: The frontend is built using React, providing a dynamic and responsive interface for users. It interacts with the server through RESTful APIs to perform CRUD operations and manage state.
- **Server**: The backend, built on Node.js and Express, handles all business logic, data processing, and interactions with the MongoDB database.

### Service-Based Architecture
The backend services are modular, each responsible for a specific aspect of the application:

- **User Management**: Handles user registration, authentication, and session management.
- **Event Management**: Manages all CRUD operations related to events.
- **Notification Service**: Sends emails to users based on their interactions with the application, such as RSVPs and event updates.

## Design Decisions

### Switch from gRPC to REST
Initially, the project considered using gRPC due to its high performance and efficient communication between services. However, the team opted to switch to RESTful APIs for the following reasons:

- **Broad Compatibility**: REST APIs are universally accessible, making them easier to consume by a wide range of clients, including web browsers and mobile devices.
- **Simplicity**: REST's reliance on the familiar HTTP protocol makes implementation and usage more straightforward.
- **Interoperability**: RESTful APIs are language and platform agnostic, allowing seamless integration with various technologies.
- **Better Fit for Web Applications**: REST aligns well with web development patterns, particularly with React's emphasis on stateless components.

### Why OOP Was Not Used
Object-Oriented Programming (OOP) was not chosen for this project due to the following reasons:

- **Statelessness**: RESTful APIs are stateless by design, which conflicts with the stateful nature of OOP. The project required a stateless approach for better scalability and performance.
- **Functional Paradigm**: JavaScript's functional programming features were preferred for their modularity and maintainability.
- **Simplicity**: The project's data model was straightforward, not requiring the complexities introduced by OOP.

## Getting Started

### Prerequisites
- **Node.js** and **npm**: Ensure you have Node.js and npm installed on your local system.
- **MongoDB**: A running instance of MongoDB (local or cloud) is required for the backend.

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/EventSphere.git
   cd EventSphere
   ```

2. **Setup the Backend**:
   - Navigate to the backend directory:
     ```bash
     cd backend
     ```
   - Install the dependencies:
     ```bash
     npm install
     ```
   - Create a `.env` file in the `backend` folder with the necessary environment variables, including your Nodemailer secrets.
   - Start the backend server:
     ```bash
     node server.js
     ```

3. **Setup the Frontend**:
   - Navigate to the frontend directory:
     ```bash
     cd frontend
     ```
   - Install the dependencies:
     ```bash
     npm install
     ```
   - Start the frontend development server:
     ```bash
     npm run start
     ```

4. **Access the Application**:
   - Open your web browser and navigate to `http://localhost:3000` to view the application.

### Usage
Once the application is running, you can explore various features:

- **Sign up** or **log in** to start creating or attending events.
- Browse the homepage to discover featured events.
- Organize events by adding details, inviting participants, and managing RSVPs.
- Attend events by registering from the event page, leaving reviews, and staying updated with notifications.

## Conclusion
EventSphere is a robust and scalable solution for event management, built using modern web technologies. Its use of the MERN stack, along with a focus on performance, security, and user experience, makes it an ideal project to showcase your full-stack development skills.





