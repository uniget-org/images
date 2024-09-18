#syntax=docker/dockerfile:1.10.0@sha256:865e5dd094beca432e8c0a1d5e1c465db5f998dca4e439981029b3b81fb39ed5

FROM cgr.dev/chainguard/wolfi-base:latest@sha256:7574456f268bc839ac78828865087c04a4297ca226b0eb5d051d4222e7690081 AS base
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