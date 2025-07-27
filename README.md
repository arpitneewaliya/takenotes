# Take Notes App

The Take Notes App is a full-stack web application designed for seamless note and task management. It provides a user-friendly interface for creating, editing, completing, and deleting notes, with all data persistently stored in a MongoDB database. The application is built with a modern technology stack, ensuring a responsive and efficient user experience.

## Features

* **Create Notes:** Easily add new notes or tasks.
* **Edit Notes:** Modify existing notes to update their content.
* **Toggle Completion Status:** Mark notes as completed or uncompleted.
* **Delete Notes:** Remove notes that are no longer needed.
* **Persistent Storage:** All notes are securely stored in a MongoDB database.
* **Responsive User Interface:** Built with Tailwind CSS for a clean and adaptive design across various devices.

## Technologies Used

The project is divided into two main parts: the frontend and the backend.

### Frontend

* **React**: A JavaScript library for building user interfaces. (v19.1.0)
* **Vite**: A fast frontend build tool that provides a rapid development experience. (v7.0.4)
* **Tailwind CSS**: A utility-first CSS framework for rapidly styling the application. (v4.1.11)
* **Axios**: A promise-based HTTP client for making API requests to the backend. (v1.11.0)
* **React Icons**: A collection of popular icon packs for React projects. (v5.5.0)
* **ESLint**: For code linting to maintain code quality and consistency.

### Backend

* **Node.js**: JavaScript runtime environment.
* **Express**: A fast, unopinionated, minimalist web framework for Node.js. (v5.1.0)
* **Mongoose**: An ODM (Object Data Modeling) library for MongoDB and Node.js. (v8.16.5)
* **MongoDB**: A NoSQL database used for storing application data.
* **Dotenv**: For loading environment variables from a `.env` file. (v17.2.1)
* **CORS**: Middleware to enable Cross-Origin Resource Sharing. (v2.8.5)
* **Nodemon**: A utility that automatically restarts the Node.js application when file changes are detected (development only). (v3.1.10)

## Setup and Installation

Follow these steps to set up and run the project locally on your machine.

### Prerequisites

* Node.js (LTS version recommended)
* npm (Node Package Manager) or Yarn
* MongoDB (running locally or a cloud-hosted instance like MongoDB Atlas)

### Steps

1.  **Clone the Repository:**

    ```bash
    git clone <repository_url>
    cd takenotes
    ```

2.  **Install Backend Dependencies:**

    Navigate to the root directory of the project and install the backend dependencies:

    ```bash
    npm install
    ```

3.  **Install Frontend Dependencies:**

    Install the frontend dependencies by running the following command from the root directory:

    ```bash
    npm install --prefix frontend
    ```

4.  **Create Environment File:**

    Create a `.env` file in the `backend/` directory with the following content:

    ```dotenv
    MONGO_URI="your_mongodb_connection_string"
    PORT=5000
    ```

    * Replace `"your_mongodb_connection_string"` with your actual MongoDB connection string (e.g., `mongodb://localhost:27017/takenotes` for local, or your Atlas URI).

## Running the Application

### Development Mode

To run the application in development mode (with hot-reloading for frontend and auto-restarts for backend):

1.  **Start the Backend Server:**
    Open a terminal in the root directory and run:

    ```bash
    npm run dev
    ```

    This will start the backend server, typically on `http://localhost:5000`.

2.  **Start the Frontend Development Server:**
    Open a **new** terminal in the root directory and run:

    ```bash
    npm run dev --prefix frontend
    ```

    This will start the frontend development server, usually on `http://localhost:5173`. The frontend is configured to proxy API requests to the backend.

### Production Build

To create a production-ready build of the application:

From the root directory, run:

```bash
npm run build