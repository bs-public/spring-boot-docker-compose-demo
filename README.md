# Spring Boot Docker Compose Demo

**Spring Boot’s native Docker Compose support** for managing infrastructure dependencies (like MySQL) during local development.

---

## Prerequisites

- Spring Boot (3.1+)
- The `docker compose` or `docker-compose CLI` application must be present on the path.

---

## For managing the Container Lifecycle

```properties
spring.docker.compose.lifecycle-management=start-and-stop
```

### Options
  - **none**: Do not start or stop Docker Compose. Manage containers manually.

  - **start-only**: Starts Docker Compose when the app starts, but does not stop it on JVM exit.

  - **start-and-stop**: Starts Docker Compose when the app starts and stops it automatically when the JVM exits.

---

##  REST API
Add User
```
curl -X POST http://localhost:8080/users -H "Content-Type: application/json" -d "{\"name\":\"Test\"}"
```

Get All Users
```
curl http://localhost:8080/users
```
