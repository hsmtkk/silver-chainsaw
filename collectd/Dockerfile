FROM ubuntu:20.04

RUN apt-get -y update \
 && apt-get -y install collectd \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["/usr/sbin/collectd", "-f"]
