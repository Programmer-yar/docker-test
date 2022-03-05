# Docker
- A way to package software so that it can run on any OS
- Can replace VM. Run different OS on top of a single OS

### Dockerfile
- A blue print for building a docker image
- Every instruction in this file is considered step or layer.
- In order to be effecient docker usually caches the layers if nothing is changed.
- Get the officially supported 'python3' image:
  `FROM python:3`
- Add app source code to the image like cd into a directory:
  `WORKDIR /code`

### Image
- A template for running docker container
- Defines the environment specific to an application
- Same environment can be recreated if you have the image
- Images can be uploaded to cloud/ repositries

### Container
- A runnable instance of the image.
- Each container should run only one process.
- Multiple containers for multiple processess.

### docker-compose
- A tool used for running multiple docker containers at the same time.
- `services` object contains keys and each key represents different containers.
  - `web` key contains settings related to app **container**
    - `build: .` use this to point towards current working directory.
    - `ports:` contains port forwarding condition
  - `db` key contains settings related to database **container**

### Commands
- Get the list of all running containers on a system:
	- `docker ps`
- Start the containers listed in 'docker-compose.yml'
  - `docker-compose up`
  - Use this command in the directory containing docker-compose.yml
- Check the port of the container
  - `docker port <container_name> or <CONTAINER ID>`
- Get the list of images on your system
  -  `docker images`


## Basic concepts to advanced concepts docker
[documentation link](https://github.com/docker/labs/tree/master/beginner/)