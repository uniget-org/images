#syntax=docker/dockerfile:1.8.0@sha256:d6d396f3780b1dd56a3acbc975f57bd2fc501989b50164c41387c42d04e780d0

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