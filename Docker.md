**Docker** is image is read-only template that contains a set of instructions for creating a set of instructions for creating a container that can run on the Docker platform.

Docker have multiple layers.

Writable layers

# Docker Basic Commands
docker  -version<br/>
docker login<br/>
docker search<br/>
docker pull<br/>
docker inspect<br/>
docker Images<br/>

docker create<br/>
docker start<br/>
docker stop<br/>

docker run<br/>
docker ps<br/>
docker ps -a<br/>
docker kill<br/>
docker exec<br/>

docker rm<br/>
docker rmi<br/>

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


