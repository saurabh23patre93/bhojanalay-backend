# Bhojanalay Backend

A Spring Boot-based backend API for the Bhojanalay food delivery/restaurant platform.

## Prerequisites

- **Java 21**
- **Maven 3.6+**
- **PostgreSQL 12+**
- **Git**

## Tech Stack

- **Framework**: Spring Boot 4.1.0
- **Database**: PostgreSQL
- **ORM**: JPA/Hibernate
- **Security**: Spring Security with OAuth2 Resource Server
- **API Documentation**: SpringDoc OpenAPI (Swagger UI)
- **Build Tool**: Maven
- **Java Version**: 21

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/saurabh23patre93/bhojanalay-backend.git
cd bhojanalay-backend
```

### 2. Configure Database

Update `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/bhojanalay_db
spring.datasource.username=postgres
spring.datasource.password=your_password
```

### 3. Build the Project

```bash
mvn clean install
```

### 4. Run the Application

```bash
mvn spring-boot:run
```

The server will start on **http://localhost:8080**

## API Documentation

Access Swagger UI for interactive API documentation:

- **Swagger UI**: http://localhost:8080/swagger-ui.html
- **OpenAPI JSON**: http://localhost:8080/v3/api-docs

## Project Structure

```
bhojanalay-backend/
├── src/
│   ├── main/
│   │   ├── java/com/bhojanalay/
│   │   │   ├── BhojanalayBackendApplication.java
│   │   │   └── config/
│   │   │       └── SecurityConfig.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/com/bhojanalay/
├── pom.xml
└── README.md
```

## Key Features

- ✅ RESTful API endpoints
- ✅ PostgreSQL database integration
- ✅ Spring Security with OAuth2 support
- ✅ JPA/Hibernate ORM
- ✅ API documentation with Swagger UI
- ✅ Input validation
- ✅ Comprehensive logging

## Development

### Build
```bash
mvn clean build
```

### Run Tests
```bash
mvn test
```

### Run with DevTools (auto-reload)
```bash
mvn spring-boot:run
```

DevTools is enabled for faster development with automatic restart on file changes.

## Configuration Properties

Key application properties can be found in `src/main/resources/application.properties`:

- `spring.application.name`: Application name
- `server.port`: Server port (default: 8080)
- `spring.datasource.url`: Database connection URL
- `spring.jpa.hibernate.ddl-auto`: Hibernate schema update strategy (update/create/validate)
- `logging.level.*`: Log level configuration

## Security

The application uses Spring Security with OAuth2 Resource Server. Security configuration is managed in `SecurityConfig.java`.

## Database

- **Type**: PostgreSQL
- **DDL Strategy**: Update (auto-creates tables on startup)
- **SQL Logging**: Enabled (DEBUG level)

## Troubleshooting

### PostgreSQL Driver Not Found
Ensure PostgreSQL dependency is in `pom.xml`:
```xml
<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
    <scope>runtime</scope>
</dependency>
```

### Swagger Not Accessible
Ensure `SecurityConfig.java` permits Swagger endpoints:
- `/swagger-ui/**`
- `/v3/api-docs/**`
- `/swagger-ui.html`

### Database Connection Failed
Verify PostgreSQL is running and credentials are correct in `application.properties`.

## Dependencies

Key dependencies:
- `spring-boot-starter-data-jpa`: JPA data access
- `spring-boot-starter-security`: Spring Security
- `spring-boot-starter-validation`: Bean validation
- `spring-boot-starter-webmvc`: REST API support
- `springdoc-openapi-starter-webmvc-ui`: Swagger UI
- `postgresql`: PostgreSQL JDBC driver
- `lombok`: Reduce boilerplate code

## Future Enhancements

- [ ] Implement Spring AI integration for intelligent features
- [ ] Add Redis caching layer
- [ ] Implement comprehensive audit logging
- [ ] Add integration tests
- [ ] Deploy to production (Docker, Kubernetes)

## License

This project is proprietary and confidential.

## Author

Saurabh Patre

## Contact

For issues and questions, please contact the development team.
