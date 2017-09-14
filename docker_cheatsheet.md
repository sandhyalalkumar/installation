Basic idea
Containers are to Virtual Machines as threads are to processes. Or you can think of them.

-Images - stopped containers are called containers.
-Containers - Running containers are called containers 


$ docker create  [ OPTION ] --creates a container but does not start it.
$ docker rename  [ OPTION ] --allows the container to be renamed.
$ docker run     [ OPTION ] --creates and starts a container in one operation.
$ docker rm      [ OPTION ] --deletes a container
$ docker update  [ OPTION ] --updates a containers resource limits.


#commands
$ docker version
	-clinet details
	-sever details

$ docker info
	- Says how many containers got.
	- Running
	- Paused 
	- Stopped 
	Images

# List of images
$ docker images 

# Running an image/container
$ docker run hello-world
	- If the it does not find an image locally, it first pull images from docker 
	  public registry website dockerhub, after downloading it will run the docker container.

# docker to see running processes and stopped images
$ docker ps

# Pulling an image
$ docker pull <image_name> -- by default latest will be downloaded
$ docker pull <image_name>:version
$ docker pull <image_name>:latest

# Running container advanced command 
$ docker run -d --name -p 80:8080 <some_name>
	-d start the container in detached mode, run in background dont luch in the terminal.
	--name name of the container like nickname
	-p port 80:8080 ( 8080 inside the container and lunched on 80 )

# Running an Ubuntu container and its terninal instance in interactive mode and 
# open terminal 
$ docker run -it --name temp ubuntu:latest /bin/bash


