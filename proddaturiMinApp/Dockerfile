# Use official JDK base image
FROM eclipse-temurin:17-jdk-alpine

# Set working directory
WORKDIR /app

# Copy everything
COPY . .

# Package the app using Maven Wrapper
RUN ./mvnw clean package -DskipTests

# Expose the port (Spring Boot defaults to 8080)
EXPOSE 8080

# Run the jar
CMD ["java", "-jar", "target/proddaturiMinApp.jar"]
