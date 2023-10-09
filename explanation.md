# Base Images

- Web application container - I chose to use the latest Node.js image, `node:14-alpine`, as the base image for running Node.js applications and provides a stable environment.

- For the MongoDB database container, I used the official MongoDB image, `mongo:latest`. It already includes the necessary setup for a MongoDB database server.

## Dockerfile

# Use the official Node.js image as the base image to minimize the size of the image
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install application dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose port 3000 for the Node.js application
EXPOSE 3000

# Define the command to start the application
CMD ["npm", "start"]