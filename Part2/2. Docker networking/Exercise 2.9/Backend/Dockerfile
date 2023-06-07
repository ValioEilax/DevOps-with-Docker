# Use the official golang 1.16 image as the base image
FROM golang:1.16

EXPOSE 8080

# Set the working directory inside the container
WORKDIR /usr/src/app

ENV REQUEST_ORIGIN=http://localhost:5000

# Copy the source code to the working directory
COPY . .

# Build the project
RUN go build

# Run the server
CMD ["./server"]
