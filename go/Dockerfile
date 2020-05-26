FROM golang:1.14-alpine3.11

# install OS dependencies and golangci-lint
RUN apk add --no-cache bash git make curl gcc g++ musl-dev \
    && curl -sSfL https://raw.githubusercontent.com/golangci/golangci-lint/master/install.sh | sh -s -- -b $(go env GOPATH)/bin v1.27.0
