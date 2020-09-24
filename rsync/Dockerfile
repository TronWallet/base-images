FROM debian:buster

RUN apt-get update \
    && apt-get install -y ca-certificates rsync --no-install-recommends \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    && update-ca-certificates

RUN addgroup gettyio \
    && adduser --disabled-password --gecos "" gettyio --uid 1000 --ingroup gettyio \
    && chown gettyio:root /etc/ssl/private

USER gettyio

ENTRYPOINT [ "/usr/bin/rsync" ]