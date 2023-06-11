# DOCKER AND DOCKER COMPOSE TUTORIAL
<!-- PROJECT LOGO -->
<br />
<div align="center">
    <img src="./assets/docker-icon.png" alt="Logo" width="100" height="100">

<h3 align="center">tutorial</h3>

  <p  align="center">
    Basic understanding and practice with docker
    <br />
    <a href="https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-22-04"><strong>How To Install and Use Docker on Ubuntu 22.04 »</strong></a>
    <br />
     <a href="https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-22-04#step-1-installing-docker-compose"><strong>How To Install and Use Docker Compose on Ubuntu 22.04 »</strong></a>
    <br />
    <br />
    <a href="">View Demo</a>
    ·
    <a href="">Report Bug</a>
    ·
    <a href="">Request Feature</a>
  </p>
</div>

# Docker

## Installing docker

```
You can visit the link  " how to install and practice with docker " and follow step 1 and step 2 to install and setup all of docker
```

## Docker command

- Main Syntax
  
```bash
docker [option] [command] [arguments]
```

- View all available subcommands:

```bash
docker 
```

- View the options available to a specific command:

```bash
docker docker-subcommand --help 
```
- View system-wide information about Docker:

```bash
docker info
```

## Docker images

- Check whether can access (If the image doesn't exists, Docker will downloaded the image from Docker Hub):

```bash
docker run [Image name]
```

- Search for images available on Docker Hub:

```bash
docker search [Image name]
```

- Download the official image:

```bash
docker pull [Image name]
```

- View Image have been downloaded:

```bash
docker images
```

## Docker container

- Run container using the lasted image of [Image name]:
  
```bash
docker run -it [image name]
```
- You cant see your cmd lock like this: ( options: d9b100f2f636 is the container id ) 
<br />
> **root@d9b100f2f636:/#**

*<sub>Now you can run any command inside the container  with root role. <sub/>*

### Managing Docker containers

- View container are running:
  
```bash
docker ps
```

- View all container:

```bash
docker ps -a
```

- View the lasted container was created:

```bash
docker ps -l
```

- Start container:

```bash
docker start [container id]
```

- Stop container:

```bash
docker stop [container name]
```

- Remove container:

```bash
docker rm [container name]
```
## Committing and Pushing

### Committing

- Committing Changes in a Container to a Docker Image:

```bash
docker commit -m "What you did to the image" -a "Author Name" [container_id] [repository]/[new_image_name]
```

### Pushing

- First log into Docker Hub:

```bash
docker login -u [docker registry username]
```

- Push your own image :

```bash
docker push [docker registry username]/[docker image name]
```