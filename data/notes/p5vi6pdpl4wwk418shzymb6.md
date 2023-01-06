# Definition
[Image vs Container](https://phoenixnap.com/kb/docker-image-vs-container)  
## Dockerfiles
Dockerfiles are a set of commands to build an image. Each command in a dockerfile adds a layer to an image.
## Images
Images are immutable snapshots of the current state, and are stored in an arbitrary number of layers. 
Images are required to run a container, and are obtained from a source like Docker hub or built with a Dockerfile.
## Container
A container refers to the environment where image layers and a read/write layer exist to run an application.

# Install
## Ubuntu Server
[Link](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)

## WSL setup
Ensure docker desktop is up to date  
wsl2 selected in docker desktop  
ubuntu installed, instance enabled in docker desktop  

### Add User / Post Install Setup
    sudo groupadd docker
    sudo usermod -aG docker $USER
    newgrp docker

## Operations
### List all containers
    docker ps -a

### Filters
    docker ps --filter "name=TEST*" 

### Stop all containers
    docker stop $(docker ps -aq)

### Start a container
    docker start CONTAINER [commands]

### Restart Policy
| Flag                     | Description                                        |
|--------------------------|----------------------------------------------------|
| no                       | Don't restart                                      |
| on-failure[:max:retries] | restart if error only. retries option is optional. |
| unless-stopped           | Like always except not if daemon restarts          |

### Startup Behaviour
Prevent single container from starting on boot
    docker update --restart=no   mycontainer

Prevent all containers from starting on boot
    docker update --restart=no $(docker ps -aq)

### Remove all containers
    docker rm $(docker ps -aq)

### Open terminal inside running container
    docker exec -it CONTAINER bash

### Copy files to/from volume
**Mount volume in container as shown but reverse the cp arguments to copy from host to container**
    docker run \  
    -v VOLUME:/dir \  
    --name copier -d hello-world \  
    docker cp copier:/dif/path /home/PATH  
    docker rm copier  

### Update all images
docker images | grep -v ^REPO | sed 's/ \+/:/g' | cut -d: -f1,2 | xargs -L1 docker pull
