FROM maven:3.9.9-eclipse-temurin-21 AS builder
WORKDIR /app
COPY . /app
RUN mvn clean package -DskipTests

FROM eclipse-temurin:21-jdk-alpine
WORKDIR /app
COPY --from=builder /app/target/profile-service.jar /app/profile-service.jar
CMD ["java", "-jar", "/app/profile-service.jar"]