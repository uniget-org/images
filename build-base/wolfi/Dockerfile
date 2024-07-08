#syntax=docker/dockerfile:1.8.1@sha256:e87caa74dcb7d46cd820352bfea12591f3dba3ddc4285e19c7dcd13359f7cefd

FROM cgr.dev/chainguard/wolfi-base:latest@sha256:2e2220cdc2bda25a2f6a27b72e2c3a240c2ed0c3ff13858d0472364f3336c0b1 AS base
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