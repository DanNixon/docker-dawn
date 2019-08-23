# DAWN in Docker

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
