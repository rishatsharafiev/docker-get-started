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