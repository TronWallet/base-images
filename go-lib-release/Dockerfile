FROM debian:buster

RUN apt-get update \
    && apt-get install -y hub bash git make ca-certificates --no-install-recommends \
    && update-ca-certificates \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

COPY --chown=root:root release.sh /usr/local/bin/