#syntax=docker/dockerfile:1.6.0

FROM ghcr.io/uniget-org/images/alpine:3.19 AS base
RUN <<EOF
apk add --update-cache --no-cache \
    autoconf \
    automake \
    libtool \
    build-base \
    pkgconf
EOF
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Alpine 3.19 + build-base" \
      org.opencontainers.image.description="Alpine 3.19 + build-base"