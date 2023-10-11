## Base Image

- Web application container - I chose to use `node:14-alpine`, as the base image for running the application.

## Dockerfile

# Use the Alpine version to minimize the size of the image
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

# Screenshot of the deployed image on DockerHub, clearly showing the version of the image
![image](https://github.com/momureithi/My-Week-4-IP-2-Project/assets/43198305/cc49ab44-3819-4337-8d7d-18d48bcc05d2)
