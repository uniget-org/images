#syntax=docker/dockerfile:1.17.1@sha256:38387523653efa0039f8e1c89bb74a30504e76ee9f565e25c9a09841f9427b05

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