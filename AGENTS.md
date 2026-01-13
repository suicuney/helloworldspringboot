# Repository Guidelines

## Project Structure & Module Organization
- `pom.xml` defines the Maven build, Java version (21), and Spring Boot dependencies.
- `src/main/java/com/example/helloworldspringboot` holds application code.
  - `HelloWorldSpringBootApplication.java` is the Spring Boot entry point.
  - `controller/HelloController.java` contains the sample web endpoint(s).
- `src/main/resources` stores configuration such as `application.properties`.
- There is currently no `src/test/java` directory; tests should live there when added.

## Build, Test, and Development Commands
- `mvn spring-boot:run` starts the app locally using the Spring Boot plugin.
- `mvn test` runs unit tests (JUnit 5 via `spring-boot-starter-test`).
- `mvn package` builds a runnable JAR in `target/`.

## Coding Style & Naming Conventions
- Java 21 source; follow standard Spring Boot conventions.
- Indentation: 2 spaces in XML (`pom.xml`), 4 spaces in Java.
- Package naming: lower-case reverse-domain, e.g., `com.example.helloworldspringboot`.
- Class naming: PascalCase; controller classes end with `Controller`.
- Configuration keys in `application.properties` use dot-delimited lower-case names.

## Testing Guidelines
- Use JUnit 5 (provided by `spring-boot-starter-test`).
- Place tests under `src/test/java` mirroring the main package structure.
- Name tests `*Test` or `*IT` (e.g., `HelloControllerTest`).
- Run all tests with `mvn test`.

## Commit & Pull Request Guidelines
- No commit message convention is visible in this repository; use clear, imperative summaries (e.g., "Add hello endpoint tests").
- PRs should include: a short description, linked issues (if any), and a note on how to validate (e.g., commands run).
- For user-facing changes, include relevant endpoint examples or screenshots.

## Configuration Tips
- Update `src/main/resources/application.properties` for ports, profiles, or logging.
- Keep environment-specific values in external configuration when possible.
