# SECTION ONE
## INTRODUCTION TO DOCKER
### OUTLINE AND CONTENT
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

-----------------------------
# SECTION TWO
## LINUX
### OUTLINE AND CONTENT
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

### Linux File System
/ 
 - bin (binary) > programs
 - boot > all files related to booting
 - dev (devices) > the files that need to access devices. In linux, Everything is a file.
 - etc (editable text configuration) > where we have configuration files
 - home > home directory for users are stored.
 - root > home directory for root users.
 - lib > used for keeping library files like software library files
 - var (variable) > files whch are updated frequently like lock files
 - proc > includes running processes.

 ### Navigating File System
 1. pwd > print working directory
 2. ls > listing item
    - ls -1 (listing one item per row)
    - ls -l (long listing)
    - ls [path where you want to see the contents]
 3. cd > change directory
    - cd boot (relative path)
    - cd /user (absolute path-starts from the root directory) 
    - cd ~ (root directory)
 
### Manipulating Files and Directories
1. mkdir (making a directory)
2. mv [filename] [newfilename] (renaming)
3. rm [filename] (to remove files)
4. rm -r [directory name] (to remove directory)
5. touch [filename] (to create a file)

### Editing and Viewing Files
1. nano [filename]
2. cat [filename] 
3. more [filename]
4. less [filename]
5. head [filename]
6. tail [filename]

### Redirection
1. \>

### Searching for Text
grep (global regular expression print)
1. grep [rab] [filename] - case sensitive
2. grep -i [rab] [filename] - case insensitive

### Chaining Commands
1. mkdir rab; cd rab; echo done; (if one command fails, the other commands will not executed)

2. mkdir rab && cd rab && echo done; (if the first command fails, the other commands will not get executed)

3. mkdir rab || echo "directory exists" (one will execute if the one true)

### Environment Variables
1. printenv
2. printenv PATH
3. echo $PATH
4. />> (appending something to a file instead of overwriting)
5. source [filename/filepath] (to reload a file)

### Managing Processes
> Process - an instance of a running program.
1. ps (listing processes)
2. kill [process id]

### Managing Users
1. useradd (adding a user) e.g user add -m rabson
2. usermod (modifying a user)
3. userdel (deleting a user)
4. adduser (more interactive)

### Managing groups
1. grouadd [devops]
2. groups [username] (viewing user groups)

### File Permissions
1. ls -l (to check permissions)
2. chmod u+x (execute permission for user)

### Packages
1. apt list (see packages in the apt database)
2. apt update 
3. apt install [package name]
4. apt remove [package name]
-----------------------------
# SECTION THREE
## BUILDING IMAGES
### OUTLINE AND CONTENT
1. Creating Docker files
2. Versioning images
3. Sharing images
4. Saving and loading images
5. Reducing the image size
6. Speeding up builds
### Dockerfile Instructions
1. FROM
2. WORKDIR
3. COPY
4. ADD
5. RUN
6. ENV
7. EXPOSE
8. USER
9. CMD
10. ENTRYPOINT

### Removing Images
1. docker image prune (removing dangling images)
2. docker container prune (removing dangling container)
3. docker image rm [name]or[imageid]

### Tagging Images
1. docker build -t react-app:1 .
2. docker image remove react-app: 1 .
3. docker image tag react-app:latest react-app: 1 
4. docker image tag [imageid] react-app:latest
-----------------------------
# SECTION FOUR
## CONTAINERS
### OUTLINE AND CONTENT
1. Starting & stopping containers
2. Publishing ports
3. Viewing logs
4. Executing commands in containers
5. Removing containers
6. Persisting data using volumes
7. Sharing source code

### Viewing logs
1. docker logs [container id]

### publishing ports
1. docker run -d -p 80:30000 --name react-app 

### executing commands in running containers
1. docker exec [c1] [ls]
2. docker exec [it] [c1] [sh]

### starting and stopping containers
1. docker start [c1]
2. docker stop [c1]

>NOTE: docker run is used to start a new container, while start is used to power up a container which was initially stopped.

### Removing containers
1. docker container rm c1 or docker rm c1
2. docker rm -f c1 

-----------------------------
### Some Docker Commands
1. docker version (checking docker version)

2. docker images or docker image ls (listing docker images)

3. docker ps (listing running containers), docker ps -a (listing all containers including the stopped ones)

4. docker run -it [container name] (starting a container and interacting with it)

5. docker start -i [processid]

6. docker run -d [container name]
(running the container in the background i.e. detach mode)

7. docker [command] --help

