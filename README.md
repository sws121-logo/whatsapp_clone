

```markdown
# React Chat Application

## Goal of the Project

The goal of this project is to develop a real-time chat application using React.js that allows users to log in and participate in chat rooms. The app features a sidebar for selecting chat rooms and a chat interface for sending and receiving messages. It also uses React Router for navigation between different rooms and contexts to manage global state.

## Purpose of the Project

The purpose of the project is to:
- **Create a functional chat interface** where users can log in, view available chat rooms, and participate in conversations.
- **Enable multi-room chat functionality**, where each room has its own set of messages and users can navigate between rooms.
- **Demonstrate state management** by using React's `useContext` and `useReducer` to manage user login and room states globally.
- **Implement conditional rendering** to display different components based on the user's login status.

---

## Overview

This is a React-based chat application with a login screen and dynamic chat room functionality. The application uses React Router for navigation between chat rooms, and state management is handled using React’s Context API along with `useReducer`. The layout follows BEM (Block Element Modifier) naming conventions for CSS classes, keeping the structure modular and maintainable.

### Key Features:
- **User Login**: Users are required to log in before accessing the chat interface.
- **Sidebar Navigation**: A sidebar lists the available chat rooms.
- **Dynamic Chat Rooms**: Users can enter different chat rooms via dynamic URLs (e.g., `/rooms/:roomId`), where each room has a unique conversation.
- **Persistent Global State**: User authentication and chat room information are managed globally using React Context and `useReducer`.

## Technology Stack

- **React.js**: JavaScript library for building user interfaces, managing state, and routing.
- **React Router**: For dynamic navigation between chat rooms.
- **Context API + `useReducer`**: For global state management of user login and application data.
- **CSS (BEM Naming)**: Organized styling for the components.

---

## Installation and Setup

To run this project locally, follow the steps below:

### Prerequisites:
- Node.js and npm installed on your local machine.

### Steps to Run:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/react-chat-app.git
   cd react-chat-app
   ```

2. **Install Dependencies**:
   Install the necessary packages by running:
   ```bash
   npm install
   ```

3. **Run the Application**:
   Start the development server:
   ```bash
   npm start
   ```
   This will open the application in your browser at `http://localhost:3000`.

## Project Structure

```bash
.
├── public
│   └── index.html         # Main HTML template
├── src
│   ├── App.js             # Main React component
│   ├── Sidebar.js         # Sidebar component displaying chat rooms
│   ├── Chat.js            # Chat room interface
│   ├── Login.js           # Login component for user authentication
│   ├── StateProvider.js   # Context and state management setup
│   ├── App.css            # Global styles following BEM conventions
│   └── index.js           # Entry point for the React app
└── package.json           # Project dependencies and scripts
```

### Core Components

1. **`App.js`**: 
   - Handles the main application structure and routing. It conditionally renders the `Login` component if the user is not logged in and the chat interface if the user is authenticated.
   
2. **`Sidebar.js`**: 
   - Displays a list of chat rooms that users can join. It uses React Router's `Link` to navigate between chat rooms.

3. **`Chat.js`**: 
   - The chat interface for sending and receiving messages in the selected room. This component dynamically updates based on the `roomId` in the URL.

4. **`Login.js`**: 
   - Handles user authentication and updates the global state when a user logs in.

5. **`StateProvider.js`**:
   - Implements React’s Context API and `useReducer` to manage the global state of the app, including user login information and chat room data.

### Example App Flow:

1. **Login**: When a user visits the app, they are greeted with the `Login` component. Once logged in, the chat interface becomes available.
   
2. **Navigate to Chat Rooms**: After logging in, the user can use the sidebar to select different chat rooms.

3. **Chat Interface**: Upon selecting a room, the `Chat` component is displayed. The chat room is identified by a dynamic URL parameter (`roomId`).

---

## Usage

1. **Login**: Once the app is loaded, log in using the provided login form.
2. **Navigate Rooms**: Use the sidebar to switch between different chat rooms.
3. **Chat**: Type messages in the chat box to participate in the room conversation.

## Future Enhancements

- **Real-time Messaging**: Integrate WebSocket or Firebase to enable real-time chat functionality.
- **Message Persistence**: Store and retrieve messages from a database to ensure conversations are not lost after refreshing the page.
- **User Authentication**: Implement real user authentication using OAuth or a custom backend for enhanced security.

---

## License

This project is licensed under the MIT License. Feel free to modify and use it for your own needs.
```

