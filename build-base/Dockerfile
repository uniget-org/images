#syntax=docker/dockerfile:1.14.0@sha256:4c68376a702446fc3c79af22de146a148bc3367e73c25a5803d453b6b3f722fb

ARG VERSION
FROM registry.gitlab.com/uniget-org/images/alpine:${VERSION} AS base
RUN <<EOF
apk add --update-cache --no-cache \
    autoconf \
    automake \
    libtool \
    build-base \
    pkgconf
EOF

ARG VERSION
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Alpine ${VERSION} + build-base" \
      org.opencontainers.image.description="Alpine ${VERSION} + build-base"