# SECTION ONE
## OUTLINE
### 1. What Is Docker
> A platform for building, running and shipping applications.

### 2. Virtual Machine VS Containers
#### Container
> An Issolated environment for running application.
1. Allow running multiple apps in isolation.
2. Are lightweight
3. Use OS of the host
4. Start quickly
5. Need less hardware resources
#### Virtual Machine
> An abstraction of a machine (physical hardware)

##### Hypervisor
> ###### A software that we use to create and manage a virtual machine. Examples include:
> ###### 1. Virtual Box
> ###### 2. VMware
> ###### 3. Hyper-v (Windows Only)

##### Problems of VM
> ###### 1. Each VM needs a full-blown OS
> ###### 2. Slow to start
> ###### 3. Resource intensive

### 3. Architecture of Docker
> Uses client-server architecture 
1. Client --REST API--> Server (Docker Engine)
> A kernel manages applications and hardware resources.

### 4. Development Workflow
1. Dockerlize (using dockerfile)
> Dockerfile is a plain text file that includes instructions that docker uses to package of its application into an image. An image contains the following:
- A cut-down OS
- A runtime environment (e.g Node)
- Application files
- Third-party libraries
-  Environment variables

2. Container

### Linux Distributions
### Distros (Some)
1. Ubuntu
2. Debian
3. Alpine
4. Fedora
5. CentOS

### Running Linux
1. docker run ubuntu (if not available it will be pulled).

### Package managers
1. apt - advanced package tool
2. apt-get

### Some Linux Commands
1. apt list (see packages in the apt database)
2. apt update 
3. apt install [package name]
4. apt remove [package name]



### Some Docker Commands
1. docker version (checking docker version)

2. docker images or docker image ls (listing docker images)

3. docker ps (listing running containers), docker ps -a (listing all containers including the stopped ones)

4. docker run -it [container name] (starting a container and interacting with it)




