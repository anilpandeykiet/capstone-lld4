E-Commerce Microservices Project
A proof-of-concept e-commerce backend built with Spring Boot and React to demonstrate microservices architecture, event-driven communication, and full-stack observability. (Academic capstone project — M.S. in Computer Science).

Architecture
API Gateway: Single entry point for client requests, secured via Nginx + SSL and Keycloak (OAuth 2.0 / OIDC).

Product Service: Manages product catalog (MongoDB).

Order Service: Processes orders and handles synchronous calls via OpenFeign with Circuit Breakers (MySQL, Flyway).

Inventory Service: Tracks and validates stock (MySQL, Flyway).

Notification Service: Consumes Apache Kafka events to send order emails (Spring Mail).

Observability Stack: Prometheus (metrics), Loki (logs), Tempo (tracing), and Grafana (dashboards).

Tech Stack
Backend: Java 24, Spring Boot, Spring Cloud (Gateway, OpenFeign, Circuit Breaker), Spring Security

Frontend: React

Data & Messaging: MySQL, MongoDB, Apache Kafka

Auth & Infrastructure: Keycloak, Docker, Docker Compose, Nginx

Testing: Testcontainers (integration testing)

Running Locally
Prerequisites
Docker & Docker Compose

(Optional for local dev) Java 24, Node.js & npm