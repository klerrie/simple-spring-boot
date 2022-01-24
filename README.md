# About
This is simple project to show how to create a basic API using Java 11 + Maven + Spring Boot + PostgrSQL + Flyway.

- Tutorials
    - https://www.codejava.net/frameworks/spring-boot/connect-to-postgresql-database-examples
    - https://www.techgeeknext.com/spring-boot/spring-boot-flyway-example


#### Create new
- Install sdkman (sdkman installs command line, https://sdkman.io/install)
    - `curl -s "https://get.sdkman.io" | bash`
    - `source "$HOME/.sdkman/bin/sdkman-init.sh"`
    - `sdk version` -> should print version
- Install spring: `sdk install springboot`
- Create new project: `spring init --dependencies=web,data-jpa first-mvn`


#### Install a JDBC (required to start server)
- To avoid database setup, add this to main: `@SpringBootApplication(exclude = {DataSourceAutoConfiguration.class })`
- To connect to PostgrSQL: https://www.codejava.net/frameworks/spring-boot/connect-to-postgresql-database-examples


#### Useful commands
- Start server dev mode: `mvn spring-boot:run`
- Install pom stuff and skip tests: `mvn clean install -DskipTests`
- Only install dependencies: `mvn dependency:resolve`


#### Organization
- Controller (@RestController) -> Service (@Service) -> Dao (@Repository) -> Repo (@Repository) -> Entity (@Component)


#### Todo (maybe)
- Maybe setup testContainers for creating a test database.
https://www.baeldung.com/spring-boot-testcontainers-integration-test

- Use @ControllerAdvice instead of using try/catch blocks in controllers
