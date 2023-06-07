# Use the official Node.js 16 Alpine base image
FROM node:16-alpine

EXPOSE 5000

# Set the working directory inside the container to /usr/src/app
WORKDIR /usr/src/app

ENV REACT_APP_BACKEND_URL=http://localhost/api/

# Copy the entire current directory into the container's working directory
COPY . .

# Install the Node.js dependencies defined in package.json
RUN npm install

# Build the project (assuming you have a build script defined in package.json)
RUN npm run build

# Install the 'serve' package globally using npm
RUN npm install -g serve

# Start the 'serve' command with options:
# -s: serve the static files from the 'build' directory
# -l: specify the listening port as 5000
CMD [ "serve", "-s", "build", "-l", "5000" ]
