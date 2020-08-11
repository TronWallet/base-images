FROM tronwallet/go:1.14-buster

RUN apt update \
    && apt-get install -y hub zip unzip bash git make ca-certificates --no-install-recommends \
    && update-ca-certificates \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    && curl -LO https://github.com/protocolbuffers/protobuf/releases/download/v3.12.4/protoc-3.12.4-linux-x86_64.zip \
    && unzip protoc-3.12.4-linux-x86_64.zip -d /usr/local/ \
    && rm -f rotoc-3.12.4-linux-x86_64.zip \
    && go get -u github.com/golang/protobuf/protoc-gen-go \
    && go get -u github.com/googleapis/googleapis; exit 0

COPY --chown=root:root release.sh /usr/local/bin/

