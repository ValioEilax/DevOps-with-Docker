### Dockerfile for Java Spring project

```console
# Make sure you have java 8 installed
FROM openjdk:8

# Expose port 8080 for the application
EXPOSE 8080

# Set the working directory
WORKDIR /usr/src/app

# Copy the project files to the container
COPY . .

# Build the project
RUN ./mvnw package

# Run the application
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
```

### Commands to build and run the project

```console
$ docker build . -t java-spring
$ docker run -p 8080:8080 java-spring
```
