# Intelij

This images extends the official [openjdk](https://hub.docker.com/_/openjdk) by IntelliJ IDEA and Apache Maven.

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
To separate project files from Intelij setting, in this example the volumes *proj* and *data* are used.

# Tags available

| Intelij    | Java         | Maven | underlaying OS   | Tags                                 |
|:----------:|:-------------|:------|:-----------------|:-------------------------------------|
| 2019.1.3   | openJDK 11   |       | Debian Stretch   | intelij-2019.1.3--openjdk-11; latest |
| 2019.1.3   | openJDK 8    | 3.3.9 | Debian Stretch   | intelij-2019.1.3--openjdk-8          |
