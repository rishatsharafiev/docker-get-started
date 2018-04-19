# Docker Get Started

https://docs.docker.com/get-started/

# Part 1: Orientation and setup

## List Docker CLI commands
```
docker # list of commands
docker container --help # list of container's commands
```

## Display Docker version and info
```
docker --version # docker version
docker version # docker version
docker info # info about current docker system
```

## Execute Docker image
```
docker run hello-world # run command in container
```

## List Docker images
```
docker image ls # list of images that was downloaded to your machine
```

## List Docker containers (running, all, all in quiet mode)
```
docker container ls # list of running containers
docker container ls --all # list of all containers
docker container ls -aq # list of all containers in quiet mode
```

## Conclusion of part one
Containerization makes CI/CD seamless. For example:
- applications have no system dependencies
- updates can be pushed to any part of a distributed application
- resource density can be optimized.

# Part 2: Containers
```
docker build -t friendlyhello .  # Create image using this directory's Dockerfile
docker run -p 4000:80 friendlyhello  # Run "friendlyname" mapping port 4000 to 80
docker run -d -p 4000:80 friendlyhello         # Same thing, but in detached mode
docker container ls                                # List all running containers
docker container ls -a             # List all containers, even those not running
docker container stop <hash>           # Gracefully stop the specified container
docker container kill <hash>         # Force shutdown of the specified container
docker container rm <hash>        # Remove specified container from this machine
docker container rm $(docker container ls -a -q)         # Remove all containers
docker image ls -a                             # List all images on this machine
docker image rm <image id>            # Remove specified image from this machine
docker image rm $(docker image ls -a -q)   # Remove all images from this machine
docker login             # Log in this CLI session using your Docker credentials
docker tag <image> username/repository:tag  # Tag <image> for upload to registry
docker push username/repository:tag            # Upload tagged image to registry
docker run username/repository:tag                   # Run image from a registry
```

# Part 3: Services
```
netstat -tnlp
docker stack ls                                            # List stacks or apps
docker stack deploy -c <composefile> <appname>  # Run the specified Compose file
docker service ls                 # List running services associated with an app
docker service ps <service>                  # List tasks associated with an app
docker inspect <task or container>                   # Inspect task or container
docker container ls -q                                      # List container IDs
docker stack rm <appname>                             # Tear down an application
docker swarm leave --force      # Take down a single node swarm from the manager
```