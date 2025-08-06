# Use official OpenJDK 17 base image
FROM eclipse-temurin:17-jdk-jammy

# Set maintainer label
LABEL maintainer="your.email@example.com"

# Set working directory
WORKDIR /app

# Copy the built JAR file (change 'your-microservice.jar' to your actual JAR name)
COPY target/rest-service-complete-0.0.1-SNAPSHOT.jar app.jar

# Expose the port your app runs on (change 8080 if different)
EXPOSE 8081



# Entry point to run the application
ENTRYPOINT ["sh", "java -jar app.jar"]
