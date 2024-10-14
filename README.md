# images

Base images used by [uniget-org/tools](https://github.com/uniget-org/tools)

## `ubuntu:22.04`

Ubuntu 22.04 plus a few useful tools

## `build-essential:22.04`

Ubuntu 22.04 plus tools for building C/C++

## `alpine:3.19`

Alpine 3.19 plus a few useful tools

## `build-base:3.19`

Alpine 3.19 plus tools for building C/C++

## `build-base:wolfi`

Wolfi OS plus tools for building C/C++

## `systemd:ubuntu24.04`

SystemD enabled Ubuntu 24.04

The following command starts systemd in the container:

```bash
docker run \
    --interactive \
    --tty \
    --rm \
    --privileged \
    --cgroupns=host \
    --volume /sys/fs/cgroup:/sys/fs/cgroup:rw \
    ghcr.io/nicholasdille/systemd-uniget \
        bash
```
