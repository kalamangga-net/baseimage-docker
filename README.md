Debian-Base
========================================================

Docker image for research and development on [Kalamangga Network](http://www.kalamangga.net).
Forked from [Phusion's work](https://github.com/phusion/baseimage-docker).
--------------------------------------------------------

Version 0.1 was released on [Docker Hub](https://hub.docker.com/r/kalamangga/debian-base).
Feel free to pull.

This work dedicated for Debian community and Big Data on Hadoop environment research.

## How to use

```
$ docker run --rm -t -i kalamangga/debian-base /sbin/my_init -- bash -l
```

## Re-use as a base

Don't forget to `apt update` before installing any packages and clean up APT when done.

```
FROM kalamangga/debian-base
...
RUN apt update
...
RUN apt clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
...
CMD ["/sbin/my_init"]
```

## Feedback

Please feel free to send any issues related this project.


