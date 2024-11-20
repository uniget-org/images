#syntax=docker/dockerfile:1.11.1@sha256:10c699f1b6c8bdc8f6b4ce8974855dd8542f1768c26eb240237b8f1c9c6c9976

FROM cgr.dev/chainguard/wolfi-base:latest@sha256:b3dd9cf08283b959c6a0a3c833e68b2882a50129930215060154b43ae6a3e81c AS base
RUN <<EOF
apk add --update-cache --no-cache \
    bash \
    curl \
    ca-certificates \
    jq \
    binutils \
    unzip \
    xz \
    vim \
    git \
    autoconf \
    automake \
    libtool \
    build-base \
    pkgconf \
    zstd
EOF
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="wolfi + build-base" \
      org.opencontainers.image.description="wolfi + build-base"