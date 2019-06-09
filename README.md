# Intelij

This images extends the official [openjdk](https://hub.docker.com/_/openjdk) by IntelliJ IDEA.

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
  alex031544/intelij
```

# Tags available

| Intelij    | Java         | underlaying OS   | Tags    |
|:----------:|:-------------|:-----------------|:--------|
| 2019.1.3   | openJDK 11   | Debian Stretch   | intelij-2019.1.3--openjdk-11; latest |
| 2019.1.3   | openJDK 8    | Debian Stretch   | intelij-2019.1.3--openjdk-8 |
