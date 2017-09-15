Conceptually containerization is similar to virtualization. We can say containers are super light weight OS. VM model was far better than physical model. But in the current software world, the world of microservices using VM is costly affair. Containers are light weight
VM/containers which are secure and efficent.

After installing an operating system on a machine, its becomes single user space. In the method of containerization, a software convert the single user namespace into mutiple isolated and independent user spaces, which can be used for mutiple applications or micro services. The user spaces are called containers and we can install software or services. 

Each container has its own root file system. Same goes for the process tree, independent process tree. As many of containers that numbers of process trees. Process in one container can not send signal to another. It's isolation yeah. Same for the network.
Each container own its own network stack, it's own routine table.

## How is it possible ? 
There is a feature in Linux kernal called _Kernal Namespaces_ allows us do what explained in the above paragraph. Linux kernal namespaces allow us to partition various aspects of the system.

The namespaces
`pid` namespace - process
`net` namespace - networking
`mnt` namespace - file system mounting
`user` namespace - user namespace

libcontainer is the default driver for Docker system. Previously they used LXC.


## Linux container 
**Container VS virtual Machine**
**Kernal namespaces, cgroups, capabilities**

## Docker Engine
**Execution Drives: libcontainers VS LXC**
**AUFS, OverlayFS, Device Mapper**

The docker engine is also called **Docker Daemon**. It is the docker engine we install each host machine, which provide us to access all docker services. It is a standardized shipping yard. Standardized run time environment. And application portablity insanly simple.

## Docker Images
**docker build | docker images | docker inspect**
**Union mount, layring, DockerFile**

## Docker Container
**docker start | stop | restart**

Docker images are we launch the docker container from. Docker Images are **build-time** instance and Docker container are **run-time** instance of docker images. For example `docker run -it fedora /bin/bash` this command uses fedora image to run fedora container which is a light weight Operating System. Images are bit like template in virtual machine. If the image is not present locally it will first pull image from dockerhub i.e. from public image registry, and the run the docker container. We can say that running instance of docker image is docker container.

## Registries, Volumes, Networking
The images are pulled from repos which are inside Resistry. Registry are docker hub and which contains bunch of repos. The hub contains some official repos i.e. trusted repos. User can also create their repo which is called unofficial repo, mostly these are created by docker community users.

## Runing the Ubuntu container for short lived (non-interactive shell)
Let's see the command `$ docker run ubuntu  /bin/bash -c "echo 'cool content' > /temp/cool-file"`. The command run Ubuntu shell in non-interactive mode. It starts the container run the shell and command in the shell once works completed it exists the shell and container.

## Container commit
The `$ docker commit <id> <repository_name>` command create new image from the original image but it contains all the changes/update in the image.
Docker commit takes the changes we made and create new image.

## Shiping a container from Ubuntu another Docker environment
**Saving a container image to a tar file**
`$ docker save -o /tmp/fridge.tar fridge`
`$ docker save -o <output archive>.tar <image_name>` 

**Then copy this tar file to anothor OS/Location/ any machine which running docker engine**
**Loading to another machine**
`$ docker load -i /tmp/fridge.tar`
`$ docker load -i <to be imported image>.tar`

