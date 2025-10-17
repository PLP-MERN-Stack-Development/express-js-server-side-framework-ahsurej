#  Product API - Week 2 Express.js Assignment

This is a RESTful API built using **Express.js** that performs standard CRUD operations for products.  
It includes middleware for logging, authentication, validation, and proper error handling.


## All my routes and middleware are in the server.js file
---

##  How to Run the Server

1. **Clone the repository**
   ``bash
   git clone <your_repo_link>
   
   2. Navigate into the project folder
   cd Week2_Assignment

3. Install dependencies
   
npm install express 

4.Run the server

node server.js

5.Access the app

Open in browser:

http://localhost:3000


Or test routes in Postman


API Documentation
🔹 GET /api/products

Description: Fetch all products.
Response Example:
``json
[
  {
    "id": "1",
    "name": "Laptop",
    "description": "High-performance laptop with 16GB RAM",
    "price": 1200,
    "category": "electronics",
    "inStock": true
  }
]
3. GET /api/products/:id

Description: Fetch a specific product by ID.
Example URL:
http://localhost:3000/api/products/1

4. POST /api/products

Description: Create a new product.
Headers:

x-api-key: 12345
Content-Type: application/json

Request Body Example:

{
  "name": "Headphones",
  "description": "Noise-cancelling headphones",
  "price": 250,
  "category": "electronics",
  "inStock": true
}

Response Example:

{
  "id": "1",
  "name": "Laptop",
  "description": "High-performance laptop with 16GB RAM",
  "price": 950,
  "category": "electronics",
  "inStock": false
}

DELETE /api/products/:id

Description: Delete a product by ID.
Response Example:
{
  "message": "Product deleted",
  "product": {
    "id": "2",
    "name": "Smartphone",
    "description": "Latest model with 128GB storage",
    "price": 800,
    "category": "electronics",
    "inStock": true
  }
}

Middleware Implemented
| Middleware Type    | Description                                    |
| ------------------ | ---------------------------------------------- |
| **Logger**         | Logs request method, URL, and timestamp        |
| **Authentication** | Checks for valid API key in headers            |
| **Validation**     | Ensures product data is valid before saving    |
| **Error Handling** | Returns proper error messages and status codes |


Environment Variables
| Variable  | Description                | Example |
| --------- | -------------------------- | ------- |
| `PORT`    | Port for the server        | 3000    |
| `API_KEY` | API key for authentication | 12345   |


Example Request (Postman)

POST http://localhost:3000/api/products

Headers:
x-api-key: 12345
Content-Type: application/json

Body:
{
  "name": "Blender",
  "description": "Powerful kitchen blender",
  "price": 100,
  "category": "kitchen",
  "inStock": true
}

Response:
{
  "id": "generated-uuid",
  "name": "Blender",
  "description": "Powerful kitchen blender",
  "price": 100,
  "category": "kitchen",
  "inStock": true
}
Author:Jerusha

