# Docker_Commands

# What is Docker?

Docker is a platform that enables developers to package applications and their dependencies into lightweight, portable containers. These containers can run consistently across different environments, providing a consistent and reproducible way to deploy, scale, and manage software. Docker simplifies the process of software development, delivery, and deployment by isolating applications in containers, making them easily shareable and deployable across various systems.

## Table of Contents

1. [Installation](#installation)
2. [Basic Commands](#basic-commands)
3. [Container Management](#container-management)
4. [Image Management](#image-management)
5. [Networks](#networks)
6. [Volumes](#volumes)
7. [Compose](#compose)



## Installation

Follow the official Docker installation guide to install Docker on your system: [Docker Installation Guide](https://docs.docker.com/get-docker/)

## Basic Commands

### Check Docker Version
```bash
docker --version
```

### Check Docker Info
```
docker info
```

### Run Docker Hello World

```
docker run hello-world
```

## Container Management

### List Running Containers

```
docker ps
```

### List All Containers (including stopped ones)

```
docker ps -a
```

### Start a Container

```
docker start <container_id_or_name>
```

### Stop a Container

```
docker stop <container_id_or_name>
```

### Remove a Container

```
docker rm <container_id_or_name>
```

### Remove All Stopped Containers

```
docker container prune
```

## Image Management

### List Downloaded Images

```
docker images
```

### Pull an Image from Docker Hub

```
docker pull <image_name>
```

### Remove an Image

```
docker rmi <image_id_or_name>
```

### Remove All Unused Images

```
docker image prune
```

## Networks

### List Networks

```
List Networks
```

### Create a Network

```
docker network create <network_name>
```

### Remove a Network

```
docker network rm <network_name>
```

## Volumes

### List Volumes

```
docker volume ls
```
### Create a Volume

```
docker volume create <volume_name>
```

### Remove a Volume

```
docker volume rm <volume_name>
```

## Compose

### Docker Compose Up

```
docker-compose up
```

### Docker Compose Down

```
docker-compose down
```



## View Container Logs
```
docker logs <container_id_or_name>
```


