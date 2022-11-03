# Docker-Commands
basic docker commands

Basic Docker Commands

# Here are the top 10 essential docker commands

    docker - version 
    docker pull 
    docker run 
    docker ps 
    docker exec 
    docker stop 
    docker restart 
    docker kill 
    docker commit 
    docker push 
    
    Let's understand the commands along with their usage. The following are the docker basic commands for beginners 
    
# 1. docker –version

This command is used to get the current version of the docker 

Syntax: docker - -version [OPTIONS] 

By default, this will render all version information in an easy-to-read layout. 

# 2. docker pull

Pull an image or a repository from a registry 

Syntax: docker pull [OPTIONS] NAME[: TAG|@DIGEST] 

To download an image or set of images (i.e. A Repository) , Once can use docker pull command 

Example:
$ docker pull dockerimage

# 3. docker run

This command is used to create a container from an image 

Syntax : docker run [OPTIONS] IMAGE [COMMAND] [ARG...] 

The docker run command creates a writeable container layer over the specified image and then starts it using the specified command.

The docker run command can be used with many variations, One can refer to the following documentation docker run. 
# 4. docker ps

This command is used to list all the containers 

Syntax: docker ps [OPTIONS] 

The above command can be used with other options like - all or –a 

docker ps -all: Lists all containers 

Example:
$ docker ps

# 5. docker exec

This command is used to run a command in a running container 

Syntax: docker exec [OPTIONS] CONTAINER COMMAND [ARG...] 

Docker exec command runs a new command in a running container.

Refer to the following article for more detail regarding the usage of the docker exec command docker exec. 

# 6. docker stop

This command is used to stop one or more running containers. 

Syntax: docker stop [OPTIONS] CONTAINER [CONTAINER...] 

The main process inside the container will receive SIGTERM, and after a grace period, SIGKILL. The first signal can be changed with the STOPSIGNAL instruction in the container’s Dockerfile, or the --stop-signal option to docker run. 

Example:
$ docker stop my_container 

# 7. docker restart

This command is used to restart one or more containers. 

Syntax: docker restart [OPTIONS] CONTAINER [CONTAINER...] 

Example:
$ docker restart my_container

# 8. docker kill

This command is used to kill one or more containers. 

Syntax: docker kill [OPTIONS] CONTAINER [CONTAINER...] 

Example:

$ docker kill my_container

# 9. docker commit

This command is used to create a new image from the container image. 

Syntax: docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]] 

Docker commit command allows users to take an existing running container and save its current state as an image 

There are certain steps to be followed before running the command

    First , Pull the image from docker hub 
    Deploy the container using the image id from first step 
    Modify the container (Any changes ,if needed) 
    Commit the changes 

Example:

$ docker commit c3f279d17e0a dev/testimage:version3. 

# 10. docker push

This command is used to push an image or repository to a registry. 

Syntax: docker push [OPTIONS] NAME[: TAG] 

Use docker image push to share your images to the Docker Hub registry or to a self-hosted one. 

Example:

$ docker image push registry-host:5000/myadmin/rhel-httpd:lates 
