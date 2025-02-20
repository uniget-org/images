#syntax=docker/dockerfile:1.14.0@sha256:0232be24407cc42c983b9b269b1534a3b98eea312aad9464dd0f1a9e547e15a7

ARG VERSION
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

ARG VERSION
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Ubuntu ${VERSION} + build-essential" \
      org.opencontainers.image.description="Ubuntu ${VERSION} + build-essential"