#syntax=docker/dockerfile:1.9.0@sha256:fe40cf4e92cd0c467be2cfc30657a680ae2398318afd50b0c80585784c604f28

ARG VERSION=22.04
FROM ubuntu:${VERSION} AS base

SHELL [ "bash", "-o", "errexit", "-c"]
ARG DEBIAN_FRONTEND=noninteractive

COPY <<no-recommends <<no-suggests /etc/apt/apt.conf.d/
APT::Install-Recommends "false";
no-recommends
APT::Install-Suggests "false";
no-suggests

RUN <<EOF
apt-get update
apt-get --simulate dist-upgrade \
| grep "^Inst" \
| grep -i security \
| cut -d' ' -f2 \
| xargs \
    apt-get install
EOF

RUN --mount=type=cache,sharing=private,target=/var/lib/apt/lists \
    --mount=type=cache,sharing=private,target=/var/cache \
    --mount=type=cache,sharing=private,target=/var/log \
    <<EOF
apt-get update
apt-get -y install \
    git \
    curl \
    ca-certificates \
    jq \
    unzip \
    binutils \
    xz-utils \
    zstd
rm /usr/local/sbin/unminimize
EOF

LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Ubuntu ${VERSION}" \
      org.opencontainers.image.description="Base image for Ubuntu ${VERSION}"