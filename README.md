# 🏠 Airbnb Clone Project

## 🚀 Objective
The backend for the Airbnb Clone project is designed to provide a robust and scalable foundation for managing user interactions, property listings, bookings, payments, and reviews. This project mimics the core features of Airbnb, focusing on API development, database architecture, security, and deployment pipelines.

---

## 🏆 Project Goals
- **User Management:** Implement secure user registration, login, and profile features.
- **Property Management:** Enable hosts to create, edit, delete, and retrieve property listings.
- **Booking System:** Allow users to book properties and manage their bookings.
- **Payment Processing:** Securely handle transactions for bookings.
- **Review System:** Enable users to post reviews and rate properties.
- **Data Optimization:** Ensure fast and scalable data access via indexing and caching.

---

## 👥 Team Roles

| Role                 | Responsibility                                                                 |
|----------------------|----------------------------------------------------------------------------------|
| **Backend Developer** | Implement API endpoints, business logic, and integrate services.               |
| **Database Administrator** | Design and maintain efficient database schema, indexing, and backups.     |
| **DevOps Engineer**  | Set up CI/CD pipelines, monitor performance, and manage deployment processes.   |
| **QA Engineer**      | Write and execute test cases to ensure backend functionality and quality.       |

---

## ⚙️ Technology Stack

| Technology         | Purpose                                                                 |
|--------------------|-------------------------------------------------------------------------|
| **Django**         | Python-based web framework used to build backend logic and APIs.        |
| **Django REST Framework** | Provides RESTful API capabilities including serializers and viewsets.  |
| **GraphQL**        | Enables efficient and flexible data querying and mutations.             |
| **PostgreSQL**     | Relational database system for storing structured data.                 |
| **Celery**         | Asynchronous task queue for background jobs like notifications.         |
| **Redis**          | Caching layer for faster performance and session management.            |
| **Docker**         | Containerization for consistent local and production environments.      |
| **GitHub Actions** | Automates CI/CD workflows like testing, building, and deploying code.   |

---
## 🗃️ Database Design

| Entity     | Fields                                                                                 |
|------------|-----------------------------------------------------------------------------------------|
| **User**   | `id`, `username`, `email`, `password`, `is_host`, `created_at`                        |
| **Property** | `id`, `user_id`, `title`, `description`, `location`, `price`, `available_dates`     |
| **Booking** | `id`, `user_id`, `property_id`, `check_in`, `check_out`, `status`                    |
| **Review**  | `id`, `user_id`, `property_id`, `rating`, `comment`, `created_at`                    |
| **Payment** | `id`, `booking_id`, `amount`, `payment_method`, `payment_status`, `timestamp`       |

**Entity Relationships:**
- A **User** can own multiple **Properties**.
- A **Booking** belongs to one **User** and one **Property**.
- A **Review** is left by a **User** for a **Property**.
- A **Payment** is tied to one **Booking**.

---

## ✨ Feature Breakdown

### 1. **User Management**
Handles registration, login, and user profile updates securely. This enables personalized experiences and authentication for API usage.

### 2. **Property Management**
Allows hosts to add and manage listings. Includes CRUD operations on property records with location, price, and description details.

### 3. **Booking System**
Users can search and book available properties. They can also manage their bookings, including check-in and check-out info.

### 4. **Payment Processing**
Processes and records transactions. Ensures financial data integrity and enables secure booking confirmation.

### 5. **Review System**
Facilitates user-generated feedback on properties. Hosts can improve their listings based on reviews and ratings.

### 6. **Database Optimization**
Uses indexing and caching (Redis) to improve response times and reduce database load during high traffic.

---

## 🔐 API Security

Security is essential to protect data integrity and user trust.

| Security Measure       | Importance                                                                 |
|------------------------|------------------------------------------------------------------------------|
| **Authentication**     | Ensures only registered users can access or modify their data.              |
| **Authorization**      | Restricts actions based on user roles (e.g., only hosts can list properties).|
| **Rate Limiting**      | Prevents abuse and protects the API from DDoS attacks.                      |
| **Data Validation**    | Prevents malicious input and preserves backend logic.                       |
| **HTTPS/TLS**          | Ensures encrypted communication between client and server.                  |

---

## 🔁 CI/CD Pipeline

### What is CI/CD?
CI/CD (Continuous Integration and Continuous Deployment) is a development practice where code changes are automatically tested and deployed through pipelines.

### Tools Used:
- **GitHub Actions:** Automates testing, linting, and deployment workflows.
- **Docker:** Packages the application in containers for portability.
- **PostgreSQL + Redis containers:** Spun up during testing to simulate production environment.
- **Celery Workers + Beat:** For scheduled background task execution.

**Benefits:**
- Reduces manual errors.
- Ensures faster and reliable deployment.
- Encourages test-driven development (TDD) practices.

---

## 📌 REST API Endpoints Overview

### 🔹 Users
- `GET /users/` – List users  
- `POST /users/` – Create user  
- `GET /users/{id}/` – Retrieve user  
- `PUT /users/{id}/` – Update user  
- `DELETE /users/{id}/` – Delete user  

### 🔹 Properties
- `GET /properties/`  
- `POST /properties/`  
- `GET /properties/{id}/`  
- `PUT /properties/{id}/`  
- `DELETE /properties/{id}/`  

### 🔹 Bookings
- `GET /bookings/`  
- `POST /bookings/`  
- `GET /bookings/{id}/`  
- `PUT /bookings/{id}/`  
- `DELETE /bookings/{id}/`  

### 🔹 Payments
- `POST /payments/` – Process payment

### 🔹 Reviews
- `GET /reviews/`  
- `POST /reviews/`  
- `GET /reviews/{id}/`  
- `PUT /reviews/{id}/`  
- `DELETE /reviews/{id}/`  

---

## 📚 Learning Objectives
By working on this project, you'll:
- Master collaborative GitHub workflows.
- Strengthen backend development using Django and PostgreSQL.
- Understand GraphQL’s role in API flexibility.
- Gain CI/CD deployment skills.
- Learn to design and secure real-world database schemas.
- Build a scalable project portfolio piece.

---

## ✅ Requirements
- GitHub account
- Familiarity with Markdown
- Knowledge of Django, DRF, PostgreSQL/MySQL
- Understanding of Docker and CI/CD practices

---

## 📂 Repository
GitHub Repository: [airbnb-clone-project](https://github.com/waweruedwin8/airbnb-clone-project)

---

