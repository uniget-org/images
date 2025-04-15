#syntax=docker/dockerfile:1.15.0@sha256:05e0ad437efefcf144bfbf9d7f728c17818408e6d01432d9e264ef958bbd52f3

ARG VERSION
FROM registry.gitlab.com/uniget-org/images/ubuntu:${VERSION}
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