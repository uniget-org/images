#syntax=docker/dockerfile:1.8.0@sha256:d6d396f3780b1dd56a3acbc975f57bd2fc501989b50164c41387c42d04e780d0

ARG VERSION=22.04
FROM ghcr.io/uniget-org/images/ubuntu:${VERSION} AS base
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
      org.opencontainers.image.title="Ubuntu ${VERSION} + build-essential" \
      org.opencontainers.image.description="Ubuntu ${VERSION} + build-essential"