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

# Docker Commands
-docker run  '<imagename>'  Run the container\
-docker ps      List of containers\
-docker ps -a  List the containers with the previous state\
-docker Stop container name or ID  To stop the container\
-docker rm   image-name  Remove container\
-docker images \
-docker rmi -remove an image\
-grep -i FROM /root/webapp-color/Dockerfile \
-docker build \ to build image
-docker run -p 8282:8080    \
-docker volume  (Volume and bind mounts) \
-docker Network (Bridge,none,Host) \
-docker network ls\
-docker inspect \
-docker network inspect bridge \

**Steps for run application in Docker**
1. Application code and dependencies
2. The docker file is a bundle of instruction

* 


