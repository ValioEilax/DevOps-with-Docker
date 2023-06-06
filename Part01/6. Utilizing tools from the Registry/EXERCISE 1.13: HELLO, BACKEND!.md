```console
# Use the official golang 1.16 image as the base image
FROM golang:1.16

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy the source code to the working directory
COPY . .

# Set the environment variables
ENV REQUEST_ORIGIN http://localhost:5000

# Build the project
RUN go build

# Run the server
CMD ["./server"]
```
