```console
# Use the official Node.js 16 Alpine base image
FROM golang:1.16

# Expose the port on which the application will listen
EXPOSE 8080

# Set the environment variables
ENV REQUEST_ORIGIN=http://localhost:5000

# Set the working directory inside the container to /usr/src/app
WORKDIR /usr/src/app

# Copy the entire current directory into the container's working directory
COPY . .

# Build the project
RUN go build server

# Run the server
CMD ["./server"]
```
