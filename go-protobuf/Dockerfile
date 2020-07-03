FROM tronwallet/go:1.14

RUN apk add --no-cache bash git g++ make curl protobuf protobuf-dev \
    && go get -u github.com/golang/protobuf/protoc-gen-go \
    && go get -u github.com/googleapis/googleapis; exit 0
