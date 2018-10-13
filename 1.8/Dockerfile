FROM debian:stretch

MAINTAINER David Wilkie <dwilkie@gmail.com>

# make the "en_US.UTF-8" locale so freeswitch will be utf-8 enabled by default
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* \
    && localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8

ENV LANG en_US.utf8
ENV FS_MAJOR 1.8

RUN apt-get update && apt-get install -y curl gnupg \
    && curl https://files.freeswitch.org/repo/deb/freeswitch-$FS_MAJOR/fsstretch-archive-keyring.asc | apt-key add - \
    && echo "deb http://files.freeswitch.org/repo/deb/freeswitch-$FS_MAJOR/ stretch main" > /etc/apt/sources.list.d/freeswitch.list \
    && echo "deb-src http://files.freeswitch.org/repo/deb/freeswitch-$FS_MAJOR/ stretch main" >> /etc/apt/sources.list.d/freeswitch.list \
    && apt-get purge -y --auto-remove curl gnupg

RUN apt-get update && apt-get install -y freeswitch
