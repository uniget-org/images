#syntax=docker/dockerfile:1.25.0@sha256:0adf442eae370b6087e08edc7c50b552d80ddf261576f4ebd6421006b2461f12

FROM cgr.dev/chainguard/wolfi-base:latest@sha256:fdcd31a2db35958c251ea22e80cda72a8222228114e736ec7dd9c94452a2dc51 AS base
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