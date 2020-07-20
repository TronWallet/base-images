FROM node:10-buster

# install OS dependencies and golangci-lint
RUN apt update \
    && yarn global add surge \
    && export PATH=$PATH:$(yarn global bin)

ENTRYPOINT [ "surge" ]
