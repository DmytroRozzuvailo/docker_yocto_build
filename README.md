# Yocto Build

How to build:

## Prepare Docker Environment

```sh
cd doc

# build docker image
docker build . -f Dockerfile --build-arg "USER_ID=$(id -u)" --build-arg "USER_GID=$(id -g)" -t yocto_build_image:latest

# create directory for building VM
mkdir -p ~/work/build_yocto

# launch container
./run_docker.sh -w  ~/work/build_yocto -d yocto_build_image
```
