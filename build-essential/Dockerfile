#syntax=docker/dockerfile:1.17.1@sha256:38387523653efa0039f8e1c89bb74a30504e76ee9f565e25c9a09841f9427b05

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