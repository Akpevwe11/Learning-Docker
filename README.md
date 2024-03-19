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

 # to pull and push a container to Docker hub

 docker pull 

 docker push 

 # to delete an image from your computer 

 docker run --rm <Container-Name>

 # 

 docker run --rm ubuntu:18.04 cat /etc/os-release

 # To build the file you'll simply run docker build and the current direct

 docker build .

 # to see a list of all the current images 

 docker image list 

 # to see all the docker process running 

 docker ps

 # to run an image 

 docker run --rm <IMAGE-ID>

 # To stop a running container 

first run `docker ps` to see the list of running container then 

 docker s top <Container-ID>

# to disregard any cache file that might have changed 

docker build . --no-cache

docker run --rm -p 3000:3000 <Image-id>



## to get inside a container in docker 

docker exec -it <Container-ID>

