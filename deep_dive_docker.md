Conceptually containerization is similar to virtualization. We can say containers are super
light weight OS. 
VM model was far better than physical model. But in the current software world, 
the world of microservices using VM is costly affair. Containers are light weight
VM/containers which are secure and efficent.

After installing an operating system on a machine, its becomes single user space.
In the method of containerization, a software convert the single user namespace into
mutiple isolated and independent namespaces/user spaces, which can be used for mutiple
applications or micro services. The namespaces are called containers and we can 
install software or services. 

Each container has its own root file system. Same goes for the process tree, independent
process tree. As many of containers that numbers of process trees. Process in one container
can not send signal to another. It's isolation yeah. Same for the network.
Each container own its own network stack, it's own routine table. 

## Linux container 
**Container VS virtual Machine**
**Kernal namespaces, cgroups, capabilities**

## Docker Engine
**Execution Drives: libcontainers VS LXC**
**AUFS, OverlayFS, Device Mapper**

## Docker Inmages
**docker build | docker images | docker inspect**
**Union mount, layring, DockerFile**

## Docker Container
**docker start | stop | restart**

## Registries, Volumes, Networking

