#syntax=docker/dockerfile:1.18.0@sha256:dabfc0969b935b2080555ace70ee69a5261af8a8f1b4df97b9e7fbcf6722eddf

ARG VERSION
FROM registry.gitlab.com/uniget-org/images/ubuntu:${VERSION} AS base
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

ARG VERSION
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Ubuntu ${VERSION} + build-essential" \
      org.opencontainers.image.description="Ubuntu ${VERSION} + build-essential"