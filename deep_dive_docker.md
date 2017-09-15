Conceptually containerization is similar to virtualization. We can say containers are super light weight OS. VM model was far better than physical model. But in the current software world, the world of microservices using VM is costly affair. Containers are light weight
VM/containers which are secure and efficent.

After installing an operating system on a machine, its becomes single user space. In the method of containerization, a software convert the single user namespace into mutiple isolated and independent user spaces, which can be used for mutiple applications or micro services. The user spaces are called containers and we can install software or services. 

Each container has its own root file system. Same goes for the process tree, independent process tree. As many of containers that numbers of process trees. Process in one container can not send signal to another. It's isolation yeah. Same for the network.
Each container own its own network stack, it's own routine table.

## How it is possible ? 
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

## Docker Inmages
**docker build | docker images | docker inspect**
**Union mount, layring, DockerFile**

Docker images are we launch the docker container from. Docker Images are **build-time** instance and Docker container are **run-time** instance of docker images.

## Docker Container
**docker start | stop | restart**

## Registries, Volumes, Networking

