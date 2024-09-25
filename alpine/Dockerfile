#syntax=docker/dockerfile:1.10.0@sha256:865e5dd094beca432e8c0a1d5e1c465db5f998dca4e439981029b3b81fb39ed5

ARG VERSION=3.19
FROM alpine:${VERSION} AS base
RUN <<EOF
apk add --update-cache --no-cache \
    bash \
    curl \
    ca-certificates \
    jq \
    binutils \
    findutils \
    coreutils \
    unzip \
    xz \
    less \
    vim \
    git \
    zstd
EOF

ARG VERSION
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Alpine ${VERSION} + build-base" \
      org.opencontainers.image.description="Alpine ${VERSION} + build-base"