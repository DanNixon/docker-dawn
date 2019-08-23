# DAWN in Docker

[![Docker Pulls](https://img.shields.io/docker/pulls/dannixon/dawn)](https://hub.docker.com/r/dannixon/dawn)
[![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/dannixon/dawn)](https://hub.docker.com/r/dannixon/dawn/builds)

[DAWN](https://dawnsci.org/) running in Docker.

## Usage

Run:
```bash
docker run \
  --rm \
  --env DISPLAY="$DISPLAY" \
  --volume /tmp/.X11-unix:/tmp/.X11-unix:ro \
  dannixon/dawn
```

You will more than likely want to assign some volumes to access data too.

Alternatively using [`x11docker`](https://github.com/mviereck/x11docker):
```bash
x11docker \
  --hostdisplay \
  --sharedir "$PWD" \
  dannixon/dawn \
  $@
```
