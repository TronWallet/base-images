FROM golang:1.14-alpine3.11

# install OS dependencies and golangci-lint
RUN apk add --no-cache bash git make curl gcc g++ musl-dev \
    && go get golang.org/x/lint/golint \
    && go get github.com/mitchellh/gox
