#syntax=docker/dockerfile:1.14.0@sha256:4c68376a702446fc3c79af22de146a148bc3367e73c25a5803d453b6b3f722fb

ARG VERSION
FROM ghcr.io/uniget-org/images/ubuntu:${VERSION}
ENV container=docker \
    LC_ALL=C \
    DEBIAN_FRONTEND=noninteractive
RUN <<EOF
apt-get update
apt-get -y install --no-install-recommends \
    ca-certificates \
    systemd \
    systemd-sysv \
    systemd-cron \
    dbus \
    sudo \
    dbus-user-session \
    vim \
    less
EOF
RUN <<EOF
#find /lib/systemd/system -type f -exec ls {} \; | sort
#cd /lib/systemd/system/sysinit.target.wants/
#ls | grep -v systemd-tmpfiles-setup | xargs rm -f $1
#rm -f /lib/systemd/system/multi-user.target.wants/*
#rm -f /etc/systemd/system/*.wants/*
#rm -f /lib/systemd/system/local-fs.target.wants/*
#rm -f /lib/systemd/system/sockets.target.wants/*udev*
#rm -f /lib/systemd/system/sockets.target.wants/*initctl*
#rm -f /lib/systemd/system/basic.target.wants/*
#rm -f /lib/systemd/system/anaconda.target.wants/*
#rm -f /lib/systemd/system/plymouth*
#rm -f /lib/systemd/system/systemd-update-utmp*
systemctl enable systemd-journald
systemctl set-default multi-user.target
EOF
COPY --chmod=0755 docker-entrypoint.sh /
STOPSIGNAL SIGRTMIN+3
VOLUME [ "/sys/fs/cgroup" ]
ENTRYPOINT [ "/docker-entrypoint.sh" ]