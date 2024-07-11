#syntax=docker/dockerfile:1.9.0@sha256:fe40cf4e92cd0c467be2cfc30657a680ae2398318afd50b0c80585784c604f28

ARG VERSION=3.19
FROM ghcr.io/uniget-org/images/alpine:${VERSION} AS base
RUN <<EOF
apk add --update-cache --no-cache \
    autoconf \
    automake \
    libtool \
    build-base \
    pkgconf
EOF
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Alpine ${VERSION} + build-base" \
      org.opencontainers.image.description="Alpine ${VERSION} + build-base"