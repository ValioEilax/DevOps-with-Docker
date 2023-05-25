### Backend Dockerfile

```console
# Use the official Golang 1.16 base image
FROM golang:1.16

# Expose port 8080 for the application
EXPOSE 8080

# Set the REQUEST_ORIGIN environment variable to http://localhost:5000
ENV REQUEST_ORIGIN=http://localhost:5000

# Set the working directory inside the container to /usr/src/app
WORKDIR /usr/src/app

# Copy the current directory's contents to the container's working directory
COPY . .

# Build the server executable
RUN go build server

# Run the server when the container starts
CMD ["./server"]
```
