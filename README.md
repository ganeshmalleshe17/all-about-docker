# all-about-docker

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
```
