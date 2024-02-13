#syntax=docker/dockerfile:1.6.0

FROM alpine:3.19 AS base
RUN <<EOF
apk add --update-cache --no-cache \
    bash \
    curl \
    ca-certificates \
    jq \
    binutils \
    unzip \
    xz \
    less \
    vim \
    git
EOF
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Alpine 3.19 + build-base" \
      org.opencontainers.image.description="Alpine 3.19 + build-base"