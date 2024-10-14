# images

Base images used by [uniget-org/tools](https://github.com/uniget-org/tools)

## `ubuntu:24.04` / `ubuntu:22.04`

Ubuntu 22.04 / 24.04 plus a few useful tools

## `build-essential:24.04` / `build-essential:22.04`

Ubuntu 22.04 / 24.04 plus tools for building C/C++

## `alpine:3.19` / `alpine:3.20`

Alpine 3.19 / 3.20 plus a few useful tools

## `build-base:3.19` / `build-base:3.20`

Alpine 3.19 / 3.20 plus tools for building C/C++

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

If running in WSL, you may need to enforce cgroupv2 exclusively in `.wslconfig`:

```plaintext
[wsl2]
kernelCommandLine=cgroup_no_v1=all systemd.unified_cgroup_hierarchy=1
```
