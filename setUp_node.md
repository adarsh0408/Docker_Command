# Set-Up NodeJs Project

## Create a Node.js Project:

```
mkdir my-node-app
cd my-node-app
npm init -y
```

## Create a Dockerfile:

Create a file named Dockerfile in the project root. This file contains instructions for building the Docker image.

```
# Use an official Node.js runtime as a base image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Expose the port on which your app will run
EXPOSE 3000

# Define the command to run your application
CMD ["node", "app.js"]
```

## Build the Docker Image:

Open a terminal and navigate to your project's root directory. Run the following command to build the Docker image:

```
docker build -t my-node-app .
```

This command tells Docker to build an image using the instructions in the Dockerfile and tag it with the name my-node-app.

## Run the Docker Container:

Once the image is built, you can run a container based on that image:

```
docker run -p 3000:3000 my-node-app
```

## Access Your Node.js App:

Open your web browser and go to http://localhost:3000 to see your Node.js application running in the Docker container.