# Docker Container for the WCAG-EM Report Tool

This repository contains a [Dockerfile](https://docs.docker.com/engine/reference/builder/) to create a [Docker](https://www.docker.com/what-docker) image to build and host the [WCAG-EM Report Tool](https://github.com/w3c/wcag-em-report-tool) by the W3C.

## Installation

```bash
### 1. Clone the repository
$ git clone https://github.com/WIENFLUSS/wcag-em-report-tool-docker.git

### 2. Change directory
$ cd wcag-em-report-tool-docker/

### 3. Build the docker-compose setup
$ docker-compose build ### Here you can supply additional commands such as your own repository for testing via the build-args argument: --build-arg GITURL="<INSERT REPOSITORY URL HERE>" w3c-report-em-tool

### 4. Run the docker-compose setup
$ docker-compose up -d
```

This will give you a running instance of the [WCAG-EM Report Tool](https://github.com/w3c/wcag-em-report-tool). You can connect via your favorite browser using the URL:
`http://127.0.0.1:8089`

## Upgrade

```bash
$ docker-compose down
$ docker-compose build --no-cache  ### Here you can supply additional commands: see Installation Step 3
$ docker-compose up -d
```

## Debugging
To get the container name/id you first type

`$ docker ps`

You can access the docker container via

`$ docker exec -it <Containername or ID> /bin/bash`
