# Build stage
FROM maven:3.8.5-openjdk-17 AS build
COPY . /build
WORKDIR /build/Stripe
RUN mvn clean package -DskipTests

# Run stage
FROM openjdk:17.0.1-jdk-slim
WORKDIR /app
COPY --from=build /build/Stripe/target/*.jar /app/Stripe.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app/Stripe.jar"]