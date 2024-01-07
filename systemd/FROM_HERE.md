# [FROM HERE](https://stackoverflow.com/questions/66205286/enable-systemctl-in-docker-container)

## build image

```bash
cd systemd
docker build -t debian_test_systemd_inside_docker -f Dockerfile "."
```

## run image

```bash

docker run -it --privileged --cap-add=ALL debian_test_systemd_inside_docker

```
