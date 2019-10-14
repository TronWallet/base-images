FROM golang:1.13-alpine3.10

# install OS dependencies and golang's dep
RUN apk add --no-cache bash git make curl gcc g++ musl-dev \
    && curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh
