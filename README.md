# Use a base image
FROM node:14

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose a port
EXPOSE 3000

# Define the command to run the application
CMD ["npm", "start"]

# to create an image from a docker file
 docker build -t algofields/simple-backend .

 # to start a container from an image.

 docker run -p 4000:4000 algofileds/simple-backend

 # to list running containers 

 docker ps

 # to stop a running container 

 docker stop <Container-ID>

 

