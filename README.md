# All-about-docker

## How to install docker in ubuntu and linux server
```sh
apt update && apt install docker.io # for ubuntu
apt update && apt install docker # for linux 

```
## Docker commands 
```sh
1) systemctl status docker  #to check docker is running or not
2) docker login # login docker hub account
3) docker pull hello-world # pull the image from docker hub
4) docker images # displays images
5) docker run hello-world # used to verify that Docker is installed correctly and working properly on your system.
6) docker ps  # displays created containers
7) docker run -d --name ganesh nginx #“This command runs an Nginx container in detached mode with the name ganesh. The container runs in the background and starts the Nginx web server.
8) docker run -d -p 8080:80 --name gm httpd  #This command is used to run an Apache (httpd) web server inside a Docker container and make it accessible from the browser.
9) docker run nginx   # “Docker run creates a new container from an image and starts it.”
10) docker run -d nginx #Run container in background (detached mode)
11) docker run -d -p 8080:80 nginx #“This command maps host port 8080 to container port 80 to access the application externally.”
12) docker ps -a #“This command lists all containers including stopped ones.”
13) docker stop <container_id> #“It stops a running Docker container.
14) docker start <container_id> #It is used to restart a stopped container.”
15) docker restart <container_id> #“This command stops and starts the container again.”
16) docker rm <container_id> #It is used to delete stopped containers.
17) docker logs <container_id> #Docker logs command is used to check application logs inside the container.”
18) docker build -t myapp #“Docker build creates an image using instructions defined in a Dockerfile.”
19) docker tag myapp myrepo/myapp:v1 #“Docker tag is used to assign a version or repository name to an image.”
20) docker push myrepo/myapp:v1 # “Docker push uploads an image to Docker Hub or private registry.”
21) docker system prune #“This command cleans up unused Docker resources to free disk space.”
22) docker network ls #“It shows all available Docker networks.”
23) docker volume ls #“Docker volume ls lists all persistent volumes.”
```
## Docker file for creating java image and deploying java application
```sh
FROM eclipse-temurin:17-jdk-alpine
# run a base image which gives all require tools and dependancies

WORKDIR /app
#creating a folder where application code will be stored
COPY src/Main.java .
#copy the source code from host machine to container
RUN javac Main.java
#compile the application code
CMD ["java" , "Main"]
# run the application
```

