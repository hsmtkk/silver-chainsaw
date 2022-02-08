FROM ubuntu:20.04

ADD https://github.com/go-graphite/go-carbon/releases/download/v0.15.6/go-carbon-linux-amd64 /usr/local/bin/

RUN mv /usr/local/bin/go-carbon-linux-amd64 /usr/local/bin/go-carbon \
 && chmod 755 /usr/local/bin/go-carbon \
 && useradd carbon

ENTRYPOINT ["/usr/local/bin/go-carbon", "-daemon=false"]
