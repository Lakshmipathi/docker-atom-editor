# docker-atom-editor

## Overview

Install and run the [Atom editor](https://atom.io/) from within a Docker container.

## Building the image

Clone this repository, change into the source directory and run:

```
docker build .
```

## Running Atom

```
docker run -d -v /tmp/.X11-unix/:/tmp/.X11-unix/ \
              -v /dev/shm:/dev/shm \
              -v ${PWD}/.atom:/.atom \
              -e DISPLAY=${DISPLAY} \
              jamesnetherton/docker-atom-editor
```

