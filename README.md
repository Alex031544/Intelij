# Intelij IDEA

This images extends the official [openjdk](https://hub.docker.com/_/openjdk) by [Intelij IDEA](https://www.jetbrains.com/idea/) and [Apache Maven](https://maven.apache.org).

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
To separate project files from Intelij settings, in this example the volumes *proj* and *data* are used to made them persistant.

A ready to go run script is available with [run_intelij](run_intelij). The folder structure to use them should look like:
```
.
├── data
├── proj
└── run_intelij
```

# Tags available

| Intelij    | Java         | Maven | underlaying OS   | Tags                                 |
|:----------:|:-------------|:------|:-----------------|:-------------------------------------|
| 2019.1.3   | openJDK 13   | 3.3.9 | Alpine Linux     | intelij-2019.1.3--openjdk-13; latest |
| 2019.1.3   | openJDK 11   | 3.3.9 | Debian Stretch   | intelij-2019.1.3--openjdk-11;        |
| 2019.1.3   | openJDK 8    | 3.3.9 | Debian Stretch   | intelij-2019.1.3--openjdk-8          |
