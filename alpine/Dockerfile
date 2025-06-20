#syntax=docker/dockerfile:1.17.1@sha256:38387523653efa0039f8e1c89bb74a30504e76ee9f565e25c9a09841f9427b05

ARG VERSION
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