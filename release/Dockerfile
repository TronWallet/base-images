FROM golang:1.14-buster

RUN apt-get update \
    && apt-get install -y hub --no-install-recommends \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN go get github.com/guilhem/bump