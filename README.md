# Product API Server
/// my server.js countains all of the routes and middleware

This is the backend for a simple **Product Management API** built with **Node.js** and **Express**. It handles basic CRUD operations for products and features custom middleware for logging, authentication, validation, and advanced functionality like filtering, search, and pagination.

---

## 🚀 How to Run Your Server
s
Follow these steps to set up and run the server locally.

### Prerequisites

You must have **Node.js** and **npm** installed.

1. Project Setup

1.  **Save the code:** Ensure your server code is saved in a file named `server.js`.
2.  **Initialize and Install:** Open your terminal in the project directory and run:

    ```bash
    npm install express body-parser uuid
    ```

 2. Start the Server

Execute the `server.js` file:

```bash
node server.js
You should see the following message, confirming the server is running on port 3000:

Server is running on http://localhost:3000
3. Authentication
All API endpoints (except the root /) require an API Key for access.

Header Name: X-API-Key

Key Value: 12345

You must include the header X-API-Key: 12345 in all your requests.


