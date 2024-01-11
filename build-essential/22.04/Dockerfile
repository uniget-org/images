#syntax=docker/dockerfile:1.6.0

FROM ghcr.io/uniget-org/images/ubuntu:22.04 AS base
RUN <<EOF
apt-get update
apt-get -y install \
    autogen \
    autoconf \
    automake \
    libtool \
    build-essential \
    pkg-config
EOF
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Ubuntu 22.04 + build-essential" \
      org.opencontainers.image.description="Ubuntu 22.04 + build-essential"