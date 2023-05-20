```console
# Make sure you have java 8 installed
FROM openjdk:8

# Set the working directory
WORKDIR /usr/src/app

# Copy the project files to the container
COPY . .

# Build the project
RUN ./mvnw package

# Run the application
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]

# Expose port 8080 for the application
EXPOSE 8080
```
