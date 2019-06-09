# Intelij

# How to run:

```
xhost +

docker run \
  -it \
  --rm \
  -d \
  -e DISPLAY=unix$DISPLAY \
  -v /tmp/.X11-unix:/tmp/.X11-unix \
  -v ${PWD}/data:/data \
  -v ${PWD}/proj:/proj \
  Alex031544/intelij
```
