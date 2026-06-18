# Stack

- Java 25 LTS
- Spring Boot 4.1.0
- Maven (multi-module)
- PostgreSQL + Testcontainers
- GraalVM native-image support

# Conventions

- Package: `com.playground.<module>` (e.g. `com.playground.rest`)
- JUnit 5 throughout (no JUnit 4)
- Spotless (Palantir format) for code formatting — `mvn spotless:apply` before committing
- Lombok for getters/setters/builders
- Flyway for DB migrations under `src/main/resources/db/migration/`
- Modules depend on `common` for shared DTOs and test utilities
- `@SpringBootTest` uses test slices where possible (`@WebMvcTest`, `@DataJpaTest`, etc.)
- `application.yml` over `application.properties`
- Profile-based config: `application-{profile}.yml`
