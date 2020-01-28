# WCAG EM REPORT TOOL DOCKER

This makes use of Docker to create a container that will host the [WCAG-EM Report tool](https://github.com/w3c/wcag-em-report-tool) by the W3C.

## Installation

### Build the dockerfile

```bash
docker build -t wcag-em-report-tool .
```

### Run the container
```bash
docker run tooling -d
```
