# Go-Admin: A Powerful and Scalable Backend Solution

Go-Admin is a feature-rich backend application built with Go, providing a robust and scalable foundation for administrative dashboards, e-commerce platforms, and other data-intensive web applications. It is designed to be easy to use and customize, with a focus on performance and security.

## Features

*   **User Management:** Create, retrieve, update, and delete users.
*   **Role-Based Access Control (RBAC):** Assign roles to users and manage permissions to control access to resources.
*   **Product Management:** Manage products, including creating, updating, and deleting product information.
*   **Order Management:** View and manage customer orders.
*   **Authentication:** Secure user authentication using JWT (JSON Web Tokens).
*   **File Uploads:** Upload and manage files, such as product images.
*   **Data Export:** Export data to CSV files.
*   **Dashboard Analytics:** Visualize data with charts and graphs.

## API Documentation

The application exposes a RESTful API for managing users, roles, products, and orders.

### Authentication
*   `POST /api/register`: Register a new user.
*   `POST /api/login`: Log in a user and receive a JWT token.
*   `GET /api/user`: Get the currently authenticated user's information.
*   `POST /api/logout`: Log out the user.

### User Management
*   `GET /api/users`: Get a list of all users.
*   `POST /api/users`: Create a new user.
*   `GET /api/users/:id`: Get a specific user by ID.
*   `PUT /api/users/:id`: Update a user's information.
*   `DELETE /api/users/:id`: Delete a user.
*   `PUT /api/users/info`: Update the authenticated user's information.
*   `PUT /api/users/password`: Update the authenticated user's password.

### Role Management
*   `GET /api/roles`: Get a list of all roles.
*   `POST /api/roles`: Create a new role.
*   `GET /api/roles/:id`: Get a specific role by ID.
*   `PUT /api/roles/:id`: Update a role.
*   `DELETE /api/roles/:id`: Delete a role.

### Permission Management
*   `GET /api/permissions`: Get a list of all available permissions.

### Product Management
*   `GET /api/products`: Get a list of all products.
*   `POST /api/products`: Create a new product.
*   `GET /api/products/:id`: Get a specific product by ID.
*   `PUT /api/products/:id`: Update a product.
*   `DELETE /api/products/:id`: Delete a product.

### File Uploads
*   `POST /api/upload`: Upload a file.
*   `GET /api/uploads/:filename`: Serve an uploaded file.

### Order Management
*   `GET /api/orders`: Get a list of all orders.
*   `POST /api/export`: Export orders to a CSV file.
*   `GET /api/chart`: Get data for the dashboard chart.

## Getting Started

### Prerequisites

*   Go 1.17 or higher
*   MySQL

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/go-admin.git
    cd go-admin
    ```

2.  **Install dependencies:**
    ```bash
    go mod tidy
    ```

3.  **Configure the database:**
    Open `database/connection.go` and update the database connection string with your MySQL credentials.

4.  **Run the application:**
    ```bash
    go run main.go
    ```
The application will be running on `http://localhost:10000`.

## Running with Docker

This project includes a `Dockerfile` and `docker-compose.yaml` for easy containerization.

### Prerequisites
*   Docker
*   Docker Compose

### Instructions

1.  **Build and run the containers:**
    ```bash
    docker-compose up --build
    ```
This command will build the Go application image and start the `go-admin` and `db` services. The application will be accessible at `http://localhost:10000`.

## Testing

A Postman collection is included in the repository (`Go-Admin.postman_collection.json`) for testing the API endpoints.

### Instructions

1.  **Import the collection** into Postman.
2.  **Set up the environment** with the base URL (`http://localhost:10000`).
3.  **Run the requests** to test the different API endpoints.
The `go-admin-postman-test.JPG` image shows a sample test run.

## Dependencies

*   [Fiber](https://github.com/gofiber/fiber): A fast and expressive web framework for Go.
*   [GORM](https://gorm.io/): The fantastic ORM library for Go.
*   [GORM MySQL Driver](https://gorm.io/docs/connecting_to_the_database.html#MySQL): MySQL driver for GORM.
*   [JWT-Go](https://github.com/dgrijalva/jwt-go): A Go implementation of JSON Web Tokens (JWT).
