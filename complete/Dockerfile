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

# Set JVM options (adjust as needed)
ENV JAVA_OPTS="-Xms256m -Xmx512m -XX:+UseG1GC -XX:MaxGCPauseMillis=200"

# Create a non-root user and switch to it for security
RUN useradd -m jenkins && chown -R jenkins:jenkins /app
USER jenkins

# Entry point to run the application
ENTRYPOINT ["sh", "-c", "java ${JAVA_OPTS} -jar app.jar"]
