#syntax=docker/dockerfile:1.16.0@sha256:e2dd261f92e4b763d789984f6eab84be66ab4f5f08052316d8eb8f173593acf7

ARG VERSION
FROM registry.gitlab.com/uniget-org/images/ubuntu:${VERSION} AS base
RUN <<EOF
apt-get update
apt-get -y install \
    autogen \
    autoconf \
    automake \
    libtool \
    build-essential \
    pkg-config
EOF

ARG VERSION
LABEL org.opencontainers.image.source="https://github.com/uniget-org/images" \
      org.opencontainers.image.title="Ubuntu ${VERSION} + build-essential" \
      org.opencontainers.image.description="Ubuntu ${VERSION} + build-essential"