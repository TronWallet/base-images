FROM tronwallet/go:1.14-buster

RUN apt update \
    && apt-get install -y hub zip unzip bash git make ca-certificates python3 python3-pip gnupg2 software-properties-common --no-install-recommends \
    && apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0 \
    && apt-add-repository -u https://cli.github.com/packages \
    && apt-get install -y gh bash git make ca-certificates --no-install-recommends \
    && python3 -m pip install bump2version \
    && update-ca-certificates \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    && curl -LO https://github.com/protocolbuffers/protobuf/releases/download/v3.12.4/protoc-3.12.4-linux-x86_64.zip \
    && unzip protoc-3.12.4-linux-x86_64.zip -d /usr/local/ \
    && rm -f rotoc-3.12.4-linux-x86_64.zip \
    && go get -u github.com/golang/protobuf/protoc-gen-go \
    && go get -u github.com/googleapis/googleapis; exit 0

