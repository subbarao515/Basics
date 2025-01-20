**Docker** is image is read-only template that contains a set of instructions for creating a container that can run on the Docker platform.

Docker have multiple layers.

Writable layers

# Docker Basic Commands
```
docker  -version
docker login
docker search
docker pull
docker inspect
docker Images

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
**Steps for run application in Docker**
1. Application code and dependencies
2. The docker file is a bundle of instruction

# Docker Networking

***Bridge*** :It creates an internal network within a Single Docker Host.<br/>
***Host*** Containter shares the network stack of the docker host<br/>
***None*** :Isolated contianer fro otehr Containers <br/>

# Docker Volumes
Docker volumes are file systems that exist outside the lifecycle of a container<br/>

# Customer Docker example.
I am used Visual studio code with docker extension for this example<br/>

Example 1<b1/>
```
FROM ubuntu:24.10
LABEL maintainer="mymail@gmail.com"

RUN apt-get update && apt-get -y install apache2
EXPOSE 80

ENTRYPOINT [ "/usr/sbin/apachectl" ]
CMD ["-D","FOREGROUND"]
```
Example 2<b1/>
```
FROM ubuntu:24.10
LABEL maintainer="mymail@gmail.com"

RUN apt-get update && apt-get -y install apache2
EXPOSE 80

ENTRYPOINT [ "/usr/sbin/apachectl" ]
CMD ["-D","FOREGROUND"]
COPY index.html /var/www/html/index.html
VOLUME /var/www/html
```

# Multi Container App
```
docker run -dit -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password -e PWD=/ -v mongodb-data:/data/db --name mern_library_nginx_mongodb_1 --net library-mern-api mongo

docker run -dit -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net  library-mern-api --name mern_library_nginx_mongo-express_1 -e ME_CONFIG_MONGODB_SERVER=mern_library_nginx_mongodb_1 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_BASICAUTH_PASSWORD=admin123456 mongo-express
```
# Docker compose
Define and run multi-container applications with Docker.
