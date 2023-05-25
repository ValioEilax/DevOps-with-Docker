```console
# Use the official golang 1.16 image as the base image
FROM golang:1.16

# Expose the port on which the application will listen
EXPOSE 8080

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy the source code to the working directory
COPY . .

# Build the project
RUN go build -o server

# Set the environment variables
ENV PORT=8080
ENV REQUEST_ORIGIN=https://example.com

# Run the server
CMD ["./server"]
```
