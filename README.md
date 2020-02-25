# Docker Container for the WCAG-EM Report Tool

This repository contains a [Dockerfile](https://docs.docker.com/engine/reference/builder/) to create a [Docker](https://www.docker.com/what-docker) image to build and host the [WCAG-EM Report Tool](https://github.com/w3c/wcag-em-report-tool) by the W3C.

## Installation

```bash
### 1. Clone the repository
$ git clone https://github.com/WIENFLUSS/wcag-em-report-tool-docker.git

### 2. Change directory
$ cd wcag-em-report-tool-docker/

### 3. Build the dockerfile
$ docker build -t wcag-em-report-tool .

### 4. Run the container
$ docker run wcag-em-report-tool -d
```

This will give you a running instance of the [WCAG-EM Report Tool](https://github.com/w3c/wcag-em-report-tool). You can connect via your favorite browser. The connection information is provided by the script.

## Upgrade

```bash
### Pull in the upstream changes from https://github.com/w3c/wcag-em-report-tool to https://github.com/WIENFLUSS/wcag-em-report-tool-docker.git
### Remove the previous container:
$ docker stop wcag-em-report-tool
$ docker rm wcag-em-report-tool 

### Execute Step 1-4 from the Installation Instructions
```
