FROM ubuntu:20.04 AS builder

ADD https://github.com/go-graphite/go-carbon/releases/download/v0.15.6/go-carbon-linux-amd64 /usr/local/bin/

RUN mv /usr/local/bin/go-carbon-linux-amd64 /usr/local/bin/go-carbon \
 && chmod 755 /usr/local/bin/go-carbon

FROM gcr.io/distroless/cc-debian11 AS runtime

COPY --from=builder /usr/local/bin/go-carbon /usr/local/bin/go-carbon

ENTRYPOINT ["/usr/local/bin/go-carbon"]
