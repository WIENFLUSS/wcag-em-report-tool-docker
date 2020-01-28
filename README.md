# WCAG EM REPORT TOOL DOCKER

This makes use of Docker to create a container that will host the [WCAG-EM Report tool](https://github.com/w3c/wcag-em-report-tool) by the W3C.

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

This will give you a running instance of the [WCAG-EM Report tool](https://github.com/w3c/wcag-em-report-tool). You can connect via your favorite browser. The connection information is provided by the script.
