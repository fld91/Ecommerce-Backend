# E-Commerce Microservices Application

## Overview
This is a **microservices-based e-commerce application** built using **Java Spring Boot**. It follows best practices and design patterns to ensure scalability, maintainability, and efficiency. The application consists of three key microservices:

1. **User Service** - Manages user authentication and profiles.
2. **Product Service** - Handles product catalog and inventory.
3. **Email Service** - Sends notifications and order confirmations.

## Technologies Used
- **Java 17**
- **Spring Boot 3**
- **Spring Data JPA** (for database interactions)
- **Redis** (for caching & session management)
- **RabbitMQ/Kafka** (for async messaging)
- **Spring Security + JWT** (for authentication)
- **OpenFeign** (for service communication)
- **Docker & Docker Compose** (for containerization)

## Architecture & Design Patterns
- **Microservices Architecture**: Services are independent and loosely coupled.
- **Service Registry & Discovery**: Using **Eureka** or **Consul**.
- **API Gateway Pattern**: Using **Spring Cloud Gateway** for centralized API management.
- **Database Per Service**: Each service has its own database.
- **Event-Driven Architecture**: Uses **RabbitMQ/Kafka** for inter-service communication.
- **Circuit Breaker Pattern**: Implemented with **Resilience4J** to handle failures.

## Microservices Overview

### 1. User Service
- Handles user registration, authentication, and profile management.
- Uses **Spring Security & JWT** for authentication.
- **Database:** PostgreSQL / MySQL

### 2. Product Service
- Manages product catalog and inventory.
- Implements **Caching with Redis** to optimize performance.
- **Database:** PostgreSQL / MySQL

### 3. Email Service
- Sends email notifications (order confirmations, promotions, etc.).
- Uses **RabbitMQ/Kafka** to receive email requests from other services.

## Running the Project
### Prerequisites
- Install **Docker & Docker Compose**
- Install **Java 17** & **Maven**

### Steps to Run
```bash
# Clone the repository
git clone https://github.com/your-repo/ecommerce-microservices.git
cd ecommerce-microservices

# Start all services using Docker Compose
docker-compose up --build
```

## API Documentation
Each microservice exposes REST APIs documented using **Swagger/OpenAPI**.
- User Service: `http://localhost:8081/swagger-ui.html`
- Product Service: `http://localhost:8082/swagger-ui.html`
- Email Service: `http://localhost:8083/swagger-ui.html`

## Future Enhancements
- Implement GraphQL for flexible data fetching.
- Improve monitoring with Prometheus & Grafana.

## Contributing
Contributions are welcome! Feel free to fork the repo and submit pull requests.


