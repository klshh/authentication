# Authentication Platform

A multi-module Spring Boot application for authentication and authorization services.

## Project Structure

```
authentication-platform/
│
├── pom.xml                  <- parent pom (packaging: pom)
│
├── auth-service/
│    ├── pom.xml             <- module pom
│    └── src/main/java...
│
├── api-gateway/
│    ├── pom.xml             <- module pom
│    └── src/main/java...
│
├── event-service/
│    ├── pom.xml             <- module pom
│    └── src/main/java...
│
├── docker-compose.yml
└── README.md
```

## Modules

### auth-service
Authentication service module handling user authentication, authorization, and security.

**Port:** 8081

### api-gateway
API Gateway module for routing and managing API requests.

**Port:** 8080

### event-service
Event service module for handling events and notifications.

**Port:** 8082

## Prerequisites

- Java 17
- Maven 3.6+
- Docker (optional, for containerized deployment)

## Building the Project

To build all modules:

```bash
mvn clean install
```

To build a specific module:

```bash
cd auth-service
mvn clean install
```

## Running the Application

### Running Individual Services

**Auth Service:**
```bash
cd auth-service
mvn spring-boot:run
```

**API Gateway:**
```bash
cd api-gateway
mvn spring-boot:run
```

**Event Service:**
```bash
cd event-service
mvn spring-boot:run
```

### Running with Docker Compose

```bash
docker-compose up
```

This will start all services in containers.

## Technology Stack

- Spring Boot 3.5.7
- Spring Security
- Spring Data JPA
- Lombok
- Maven (Multi-module)

## Development

The project uses a multi-module Maven structure where:
- The parent `pom.xml` manages common dependencies and configurations
- Each module has its own `pom.xml` with module-specific dependencies
- All modules share the same parent configuration

## License

[Add your license information here]

