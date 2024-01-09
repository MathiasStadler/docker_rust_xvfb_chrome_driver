# [FROM HERE](https://stackoverflow.com/questions/66205286/enable-systemctl-in-docker-container)

## build image

```bash
cd systemd && docker build -t debian_test_systemd_inside_docker -f Dockerfile "."

cd systemd && docker build -t ubuntu_test_systemd_inside_docker -f Dockerfile_ubuntu_22_04 "."

cd systemd && docker build -t docker_ubuntu_test_systemd -f Dockerfile_ubuntu_23_10 "."
```

## run image

```bash

docker run -it --privileged --cap-add=ALL debian_test_systemd_inside_docker

docker run -it --privileged --cap-add=ALL ubuntu_test_systemd_inside_docker
docker run -it --privileged --cap-add=ALL docker_ubuntu_test_systemd
```
