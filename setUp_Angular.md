# Angular App Set-Up

## Create an Angular Project:

```
ng new my-angular-app
cd my-angular-app
```

## Create a Dockerfile:

In the root of your Angular project, create a file named Dockerfile with the following content:

```
# Use an official Node.js LTS image as a base image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Build the Angular app for production
RUN npm run build --prod

# Expose the port on which your Angular app will run
EXPOSE 80

# Define the command to start your Angular app
CMD ["npm", "start"]
```

## Build the Docker Image:

Open a terminal and navigate to your Angular project's root directory. Run the following command to build the Docker image:

```
docker build -t my-angular-app .
```

This command tells Docker to build an image using the instructions in the Dockerfile and tag it with the name my-angular-app.

## Run the Docker Container:

Once the image is built, you can run a container based on that image:

```
docker run -p 8080:80 my-angular-app
```

This command runs a container based on the my-angular-app image and maps port 8080 on your host machine to port 80 inside the container.

## Access Your Angular App:

Open your web browser and go to http://localhost:8080 to see your Angular application running in the Docker container.