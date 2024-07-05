# Microservices Project

This project is a microservices-based application that consists of three main services: **Company**, **Job**, and **Review**. Users can create, update, delete, and retrieve these entities via the APIs exposed by these services.

## Overview

The project is built using several technologies and tools to ensure scalability, resilience, and easy management. Here are the key components and technologies used:

- **Spring Boot Actuator**: For monitoring and management of the application.
- **PostgreSQL**: As the database to store entities.
- **pgAdmin**: To manage the PostgreSQL database.
- **Docker**: To containerize the application.
- **Kubernetes (K8s)**: To deploy and manage the application containers.
- **OpenFeign**: As a declarative web service client to simplify HTTP API calls.
- **Zipkin**: For distributed tracing to monitor and troubleshoot latency issues.
- **Spring Cloud Config Server**: For centralized configuration management.
- **API Gateway**: To manage and route the API requests.
- **Resilience4j**: For implementing fault tolerance.
- **RabbitMQ**: As a message broker. It is used in this project to calculate the average rating for each company by calling the Review microservice.

## Services

### Company Service

- **API Endpoints**:
  - `POST /companies` - Create a new company
  - `GET /companies/{id}` - Retrieve a company by ID
  - `PUT /companies/{id}` - Update an existing company
  - `DELETE /companies/{id}` - Delete a company

### Job Service

- **API Endpoints**:
  - `POST /jobs` - Create a new job
  - `GET /jobs/{id}` - Retrieve a job by ID
  - `PUT /jobs/{id}` - Update an existing job
  - `DELETE /jobs/{id}` - Delete a job

### Review Service

- **API Endpoints**:
  - `POST /reviews` - Create a new review
  - `GET /reviews/{id}` - Retrieve a review by ID
  - `PUT /reviews/{id}` - Update an existing review
  - `DELETE /reviews/{id}` - Delete a review

## Running the Project

### Prerequisites

- Docker
- Kubernetes
- PostgreSQL
- pgAdmin

### Steps to Run

1. **Clone the repository**:
   ```sh
   clone each projects
2. **Build and run the Docker containers**:
   ```sh
   docker-compose up
3. **Deploy to Kubernetes**:
   ```sh
   kubectl apply -f k8s/
4. **Access the Services**:
   - Use pgAdmin to manage your PostgreSQL database.
   - Use the exposed APIs to interact with the Company, Job, and Review services.
   - Monitor the application using Spring Boot Actuator endpoints.
   - Trace requests using Zipkin.
   - Manage configurations using Spring Cloud Config Server.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

© 2024 Sasiri Jambugaswaththa. All Rights Reserved.

