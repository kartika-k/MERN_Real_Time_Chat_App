# MERN_Real_Time_Chat_App-CatchUP 

A full-stack real-time chat application built using the MERN stack with WebSocket support for real-time communication. This application offers seamless one-on-one private chats, room-based group messaging, and user-friendly features like light/dark mode and responsive design.

# Overview
This application supports:

- Private Chats: Chat with other users privately in a secure environment.

- Room Chats: Create rooms to facilitate group discussions.

- Real-Time Updates: User status changes, message notifications, and room events are all updated instantly.

- Responsive UI: Works perfectly on all devices, supporting both light and dark modes.

# Technologies
- database - MongoDB
- backend - Express.js & Node.js
- frontend - React.js (with styled-components)
- Real-time messages - Socket.io

# Architecture

Application Structure
The project is structured into two main directories:

# Client:

- Built with React.js.

- Handles UI and user interactions.

Communicates with the backend via REST APIs and WebSockets.

# Server:

- Built with Node.js and Express.js.

- Manages business logic, authentication, and database interactions.

- Uses Socket.io to enable real-time communication.

# Concurrency Handling

- Socket.io: Ensures real-time updates using WebSocket connections.

- Manages simultaneous user connections efficiently.

- Broadcasts events such as user status changes and room updates to relevant clients only.

- MongoDB: Handles concurrent database operations, like storing chat history and user data, with built-in ACID compliance.
- Design Choices:
- Stateless REST APIs are combined with persistent WebSocket connections for optimal real-time communication.
- Scalable event-handling architecture ensures minimal latency during high traffic.

  # Assumptions and Design Choices
- Assumptions
- Users must sign in to access chat features.
- A user can participate in multiple chat rooms simultaneously.
- Messages are delivered only to online users in real-time. Offline users can view missed messages after logging in.
- Design Choices
- Authentication:
- Used JWT (JSON Web Tokens) for secure and stateless user sessions.
- JWT tokens expire periodically to enhance security.
- Themes and RWD:
- Chose styled-components for dynamic theme switching.
- Ensured responsive web design (RWD) for mobile-first usability.
- Real-Time Communication:
- Leveraged Socket.io for its robust event-driven model.
- Implemented event broadcasting for room-based communication.

  # Setup Instructions
Prerequisites
Ensure you have the following installed on your system:

- Node.js (v14 or above) – Download here
- MongoDB – Download here
- npm or yarn

# Follow these steps to run the application locally:

1. Clone the Repository

- git clone https://github.com/<your-username>/<your-repo-name>.git
- cd <your-repo-name>

2. Install Dependencies :
-  Backend : cd server
            npm install
- Frontend :  cd ../client
              npm install
3. Configure Environment Variables
Create a .env file in the server directory with the following:
- PORT=5000
- MONGO_URI=your_mongodb_connection_string
- JWT_SECRET=your_jwt_secret
- SOCKET_PORT=5001
- For the client, configure the backend API URL in the .env file (if needed):

REACT_APP_BACKEND_URL=http://localhost:5000

4. Start the Applications :
   Backend : cd server
             npm start
   Frontend : cd client
              npm start

Access the application at http://localhost:3000 in your browser.

# Screenshots

- Login Page : ![Screenshot 2024-11-27 205026](https://github.com/user-attachments/assets/1be3ccd6-5f14-4ce0-b655-eee4c160e831)
- Register Page (with user profile pic - optional) : ![image](https://github.com/user-attachments/assets/c9a50a03-68ec-42df-9bcc-8b13ac750d22)

- ![Screenshot 2024-11-27 205106](https://github.com/user-attachments/assets/446ca145-7c6c-46dd-91c1-c27f4edf9c1f)
- After Signup / Login :
  ![Screenshot 2024-11-27 205300](https://github.com/user-attachments/assets/596e8d9e-deeb-4110-be13-4f5a2e6cc6e0)

  ![Screenshot 2024-11-27 205434](https://github.com/user-attachments/assets/a8a4704e-05a4-4bc9-b6a1-cd3dacc66874)
- create Groups : ![Screenshot 2024-11-27 205455](https://github.com/user-attachments/assets/d71bfd94-ccf8-4b9c-be13-cc07ed2d68e2)
- ![Screenshot 2024-11-27 205619](https://github.com/user-attachments/assets/edf71ac6-0ea6-4966-bf92-24bc1ba07e65)
- creating a group : ![Screenshot 2024-11-27 205642](https://github.com/user-attachments/assets/9eab7fc3-1d12-425b-ae8d-1b35ba1ef546)
- ![Screenshot 2024-11-27 205719](https://github.com/user-attachments/assets/d1d3152c-f2bb-4242-b2eb-4254620123fb)
- user-1 Profile : ![Screenshot 2024-11-27 210008](https://github.com/user-attachments/assets/df4e67a6-a518-4a49-9b89-29abf1a33eb8)
- user-2 Profile : ![Screenshot 2024-11-27 210203](https://github.com/user-attachments/assets/b803cd68-a636-49c4-8da8-725943c91c53)

- Group Chat : ![Screenshot 2024-11-27 210051](https://github.com/user-attachments/assets/c5a65b8d-2a2b-424e-b0ca-4ca5d883ece4)
- Notifications : ![Screenshot 2024-11-27 210129](https://github.com/user-attachments/assets/c3bbd957-4135-490c-8da9-d78e778e2a49)
- Leave Group functionality : ![Screenshot 2024-11-27 210218](https://github.com/user-attachments/assets/46010d54-4dab-479c-9522-4b3f635b1ada)
- user can send emojis : ![Screenshot 2024-11-27 210927](https://github.com/user-attachments/assets/81efd501-0897-446b-982b-5cee8712d8d4)














