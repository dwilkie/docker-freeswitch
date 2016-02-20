# Supported tags and respective `Dockerfile` links

-	[`1.4.26`, `1.4`, `latest` (*1.4/Dockerfile*)](https://github.com/n42org/docker-freeswitch/blob/master/1.4/Dockerfile)

[![](https://badge.imagelayers.io/n42org/freeswitch:latest.svg)](https://imagelayers.io/?images=n42org/freeswitch:1.4.26)

# What is FreeSWITCH?

FreeSWITCH is a scalable open source cross-platform telephony
platform designed to route and interconnect popular communication
protocols using audio, video, text or any other form of media.

> [freeswitch.org](https://freeswitch.org/)

![logo](https://freeswitch.org/wp-content/themes/ken1/images/FS-new-web-logo.png)

# How to use this image.

### Create a `Dockerfile` in your project

```dockerfile
FROM n42org/freeswitch:latest
```

Then, run the commands to build and run the Docker image:

```console
$ docker build -t my-fs .
$ docker run -it --rm --name my-fs-app -v "$PWD/freeswitch":/etc/freeswitch my-fs
```

### Without a `Dockerfile`

If you don't want to include a `Dockerfile` in your project, it is sufficient to do the following:

```console
$ docker run -it --rm --name my-fs-app -v "$PWD/freeswitch":/etc/freeswitch n42org/freeswitch:latest
```

# License

View [license information](https://freeswitch.org/stash/projects/FS/repos/freeswitch/browse/docs/COPYING) for the software contained in this image.

# Supported Docker versions

This image is officially supported on Docker version 1.10.1.
