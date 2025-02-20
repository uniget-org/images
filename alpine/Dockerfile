#syntax=docker/dockerfile:1.14.0@sha256:0232be24407cc42c983b9b269b1534a3b98eea312aad9464dd0f1a9e547e15a7

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