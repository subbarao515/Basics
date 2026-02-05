# Image
An Image is a read-only, immutable template containing the application code, libraries, and environment variables. 
# Container
A Container is a live, running instance of that image.

# Docker
Docker is a platform that uses **images** (read-only templates) containing instructions to create containers that can run applications.

## Docker Layers
- Docker images have multiple layers.
- The top layer is writable; lower layers are read-only.

---

## Docker Basic Commands

```sh
docker --version
docker login
docker search
docker pull
docker inspect
docker images

docker create
docker start
docker stop

docker run
docker ps
docker ps -a
docker kill
docker exec

docker rm
docker rmi
```

---

## Steps to Run an Application in Docker
1. Prepare application code and dependencies.
2. Create a Dockerfile (a bundle of instructions for building the image).

---

## Docker Networking
- **Bridge**: Creates an internal network within a single Docker host.
- **Host**: Container shares the network stack of the Docker host.
- **None**: Isolated container from other containers.
       
    Quick Network commands

     * docker network ls 
     * docker inspect <container id>
     * docker network inspect bridge
    
---

## Docker Volumes
Docker volumes are file systems that exist outside the lifecycle of a container, allowing data persistence.

---

## Custom Docker Example
_This example uses Visual Studio Code with the Docker extension._

### Example 1
```dockerfile
FROM ubuntu:24.10
LABEL maintainer="mymail@gmail.com"

RUN apt-get update && apt-get -y install apache2
EXPOSE 80

ENTRYPOINT ["/usr/sbin/apachectl"]
CMD ["-D", "FOREGROUND"]
```

### Example 2
```dockerfile
FROM ubuntu:24.10
LABEL maintainer="mymail@gmail.com"

RUN apt-get update && apt-get -y install apache2
EXPOSE 80

ENTRYPOINT ["/usr/sbin/apachectl"]
CMD ["-D", "FOREGROUND"]
COPY index.html /var/www/html/index.html
VOLUME /var/www/html
```

---

## Multi-Container App Example
```sh
docker run -dit -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password -e PWD=/ -v mongodb-data:/data/db --name mern_library_nginx_mongodb_1 --net library-mern-api mongo

docker run -dit -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net library-mern-api --name mern_library_nginx_mongo-express_1 -e ME_CONFIG_MONGODB_SERVER=mern_library_nginx_mongodb_1 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_BASICAUTH_PASSWORD=admin123456 mongo-express
```

---

## Docker Compose
Define and run multi-container applications with Docker Compose.

---

## Docker Swarm
Docker Swarm is a container orchestration tool that enables the management, deployment, and scaling of Docker containers across a cluster of machines. Services and tasks are part of Docker Swarm.

### Features
- Centralized access
- High security
- Auto load balancing
- High scalability
- Roll-back a task

### Services
- **Replicated**: Specify the number of identical tasks you want to run.
- **Global**: Service that runs one task on every node.

### Task
- A task is the atomic unit of scheduling within a swarm.

---

