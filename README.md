# 🛒 Sales-Savvy

## Full-Stack E-Commerce Platform

Sales-Savvy is a modern **full-stack e-commerce platform** built using **Java Spring Boot, React.js, MySQL, and Docker**.

The application provides a complete shopping experience with **JWT-based authentication, product management, shopping cart functionality, order processing, RESTful APIs, and containerized deployment**.

---

## 🚀 Tech Stack

### Backend

* ☕ Java
* 🌱 Spring Boot
* 🔐 Spring Security
* 🔑 JWT Authentication
* 🌐 REST APIs
* 🗃️ Spring Data JPA
* 🛠️ Hibernate
* 📦 Maven

### Frontend

* ⚛️ React.js
* 🌐 REST API Integration
* 🎨 HTML / CSS / JavaScript

### Database

* 🐬 MySQL

### DevOps & Deployment

* 🐳 Docker
* 🐳 Docker Compose
* 🔧 Git & GitHub

---

## ✨ Features

### 🔐 Authentication & Authorization

* User Registration
* User Login
* JWT-based Authentication
* Secure API Endpoints
* Role-based Authorization
* Protected Routes

### 🛍️ Product Management

* Add Products
* Update Products
* Delete Products
* View Products
* View Product Details
* Product Price Management
* Product Inventory Management

### 🛒 Shopping Cart

* Add Products to Cart
* Remove Products from Cart
* Update Product Quantity
* View Cart
* Automatic Cart Total Calculation

### 📦 Order Management

* Place Orders
* View Orders
* View Order Details
* Order History
* Order Status Management
* Automatic Order Total Calculation

### 🔌 REST APIs

* RESTful Backend Architecture
* JSON-based Communication
* CRUD Operations
* DTO-based Data Transfer
* Exception Handling
* Layered Architecture

### 🐳 Dockerized Application

* Dockerized React Frontend
* Dockerized Spring Boot Backend
* MySQL Container
* Docker Compose
* Easy Application Setup
* Isolated Development Environment

---

# 🏗️ Application Architecture

```text
                        ┌──────────────────────┐
                        │       React.js       │
                        │      Frontend        │
                        └──────────┬───────────┘
                                   │
                                   │ REST API
                                   ▼
                        ┌──────────────────────┐
                        │     Spring Boot      │
                        │       Backend        │
                        ├──────────────────────┤
                        │    Controllers       │
                        │         ↓            │
                        │      Services        │
                        │         ↓            │
                        │    Repositories      │
                        │         ↓            │
                        │   JPA / Hibernate    │
                        └──────────┬───────────┘
                                   │
                                   ▼
                        ┌──────────────────────┐
                        │        MySQL         │
                        │       Database       │
                        └──────────────────────┘
```

---

# 📁 Project Structure

```text
Sales-Savvy/
│
├── backend/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── salessavvy/
│   │   │   │           ├── controller/
│   │   │   │           ├── service/
│   │   │   │           ├── repository/
│   │   │   │           ├── entity/
│   │   │   │           ├── dto/
│   │   │   │           ├── security/
│   │   │   │           └── config/
│   │   │   │
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   │
│   │   └── test/
│   │
│   ├── Dockerfile
│   └── pom.xml
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── context/
│   │   └── App.jsx
│   │
│   ├── Dockerfile
│   ├── package.json
│   └── package-lock.json
│
├── docker-compose.yml
├── .gitignore
└── README.md
```

# 🔐 Authentication Flow

Sales-Savvy uses **JWT (JSON Web Token)** authentication to secure protected APIs.

```text
User
 │
 │ Login
 ▼
React Frontend
 │
 │ POST Login Request
 ▼
Spring Boot Backend
 │
 │ Validate Credentials
 ▼
MySQL Database
 │
 │ User Valid
 ▼
JWT Token Generated
 │
 ▼
React Frontend
 │
 │ Store JWT
 ▼
Authenticated API Requests
 │
 │ Authorization: Bearer <token>
 ▼
Protected Spring Boot APIs
```

---

# 🔌 REST API

## 🔐 Authentication

```http
POST /api/auth/register
POST /api/auth/login
```

## 📦 Products

```http
GET    /api/products
GET    /api/products/{id}
POST   /api/products
PUT    /api/products/{id}
DELETE /api/products/{id}
```

## 🛒 Cart

```http
GET    /api/cart
POST   /api/cart
PUT    /api/cart/{id}
DELETE /api/cart/{id}
```

## 📦 Orders

```http
POST /api/orders
GET  /api/orders
GET  /api/orders/{id}
```

---

# 🖥️ Screenshots

## 🏠 Home Page

![Home Page](screenshots/home.png)

## 🔐 Login Page

![Login Page](screenshots/login.png)

## 🛍️ Products Page

![Products Page](screenshots/products.png)

## 🛒 Shopping Cart

![Shopping Cart](screenshots/cart.png)

## 📦 Orders

![Orders](screenshots/orders.png)

> Create a `screenshots` folder in the root directory and add your screenshots.

---

# 🐳 Docker Setup

The complete application is containerized using Docker.

```text
                    Docker Compose
                          │
             ┌────────────┼────────────┐
             │            │            │
             ▼            ▼            ▼
        ┌─────────┐  ┌────────────┐  ┌─────────┐
        │ React   │  │ Spring Boot│  │  MySQL  │
        │Frontend │  │  Backend   │  │Database │
        └─────────┘  └────────────┘  └─────────┘
```

---

# 🚀 Getting Started

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Sales-Savvy.git

cd Sales-Savvy
```

---

# 🐳 Run Using Docker

Make sure you have:

* Docker installed
* Docker Compose installed

Build and start the application:

```bash
docker compose up --build
```

Run in detached mode:

```bash
docker compose up -d --build
```

Check running containers:

```bash
docker ps
```

Stop the application:

```bash
docker compose down
```

---

# 💻 Run Backend Locally

Navigate to the backend:

```bash
cd backend
```

Build the project:

```bash
./mvnw clean install
```

Run Spring Boot:

```bash
./mvnw spring-boot:run
```

### Windows

```bash
mvnw.cmd spring-boot:run
```

---

# ⚛️ Run Frontend Locally

Navigate to the frontend:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

If your project uses Create React App:

```bash
npm start
```

---

# 🗄️ Database Configuration

Sales-Savvy uses **MySQL** as its relational database.

Example configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/sales_savvy
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

For Docker:

```properties
spring.datasource.url=jdbc:mysql://mysql:3306/sales_savvy
```

> Never commit real database passwords or JWT secrets to GitHub.

---

# 🔄 Application Flow

```text
                         USER
                           │
                           ▼
                    ┌─────────────┐
                    │  React.js   │
                    │  Frontend   │
                    └──────┬──────┘
                           │
                           │ HTTP / REST
                           ▼
                 ┌────────────────────┐
                 │    Spring Boot     │
                 │      Backend       │
                 └─────────┬──────────┘
                           │
             ┌─────────────┼─────────────┐
             │             │             │
             ▼             ▼             ▼
        Controllers     Services     Security/JWT
             │             │
             └──────┬──────┘
                    │
                    ▼
             Spring Data JPA
                    │
                    ▼
                 ┌───────┐
                 │ MySQL │
                 └───────┘
```

---

# 🧠 Key Concepts Demonstrated

This project demonstrates practical knowledge of:

* ☕ Core Java
* 🌱 Spring Boot
* 🔐 Spring Security
* 🔑 JWT Authentication
* 🌐 REST API Development
* 🗃️ Spring Data JPA
* 🛠️ Hibernate
* ⚛️ React.js
* 🐬 MySQL
* 🐳 Docker
* 🐳 Docker Compose
* 🔄 CRUD Operations
* 🧩 Entity Relationships
* 🏛️ Layered Architecture
* 📦 DTO Pattern
* 🚨 Exception Handling
* 🔗 Frontend-Backend Integration
* 🔧 Git & GitHub

---

# 🛡️ Security

The application implements several security mechanisms:

* JWT-based authentication
* Protected REST APIs
* Spring Security
* Role-based authorization
* Password authentication
* Unauthorized request handling

For production deployment, additional security practices such as HTTPS, secure secret management, refresh tokens, rate limiting, and input validation should be implemented.

---

# 🧪 Testing

Run backend tests using Maven:

```bash
./mvnw test
```

For Windows:

```bash
mvnw.cmd test
```

---

# 📈 Future Improvements

* 💳 Payment Gateway Integration
* ❤️ Wishlist
* 🔎 Advanced Product Search
* 🏷️ Product Categories
* 🎯 Product Filters
* ⭐ Product Reviews & Ratings
* 📧 Email Notifications
* 📊 Admin Dashboard
* 📈 Sales Analytics
* 🖼️ Cloud Image Storage
* 🔄 Refresh Token Authentication
* ⚡ Redis Caching
* ☁️ Cloud Deployment
* 🔁 CI/CD Pipeline
* 🧪 Improved Test Coverage
* 📱 Enhanced Mobile Responsiveness

---

# 📊 Project Overview

| Category         | Technology         |
| ---------------- | ------------------ |
| Frontend         | React.js           |
| Backend          | Java + Spring Boot |
| Database         | MySQL              |
| Authentication   | JWT                |
| Security         | Spring Security    |
| API              | REST               |
| ORM              | JPA / Hibernate    |
| Build Tool       | Maven              |
| Containerization | Docker             |
| Orchestration    | Docker Compose     |
| Version Control  | Git / GitHub       |

---

# 🤝 Contributing

Contributions are welcome!

### 1. Fork the repository

### 2. Create a feature branch

```bash
git checkout -b feature/new-feature
```

### 3. Commit your changes

```bash
git commit -m "Add new feature"
```

### 4. Push your branch

```bash
git push origin feature/new-feature
```

### 5. Open a Pull Request

---

# 📄 License

This project is developed for **learning, portfolio, and demonstration purposes**.

If you want to open-source this project, consider adding an appropriate license such as the **MIT License**.

---

# 👨‍💻 Author

## Pranav

### Java Full-Stack Developer

**Technologies & Interests**

```text
Java
Spring Boot
React.js
MySQL
Spring Security
JWT
REST APIs
Docker
Full-Stack Development
```

---

# ⭐ Support

If you like this project, consider giving the repository a ⭐ on GitHub!

---

<div align="center">

## 🛒 Sales-Savvy

### A complete Full-Stack E-Commerce Platform

**Built with ❤️ using Java • Spring Boot • React.js • MySQL • Docker**

⭐ Star this repository if you found it useful!

</div>
