FROM python:3.7-buster

RUN apt-get update \
    && apt-get install -y gnupg2 software-properties-common --no-install-recommends \
    && apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0 \
    && apt-add-repository -u https://cli.github.com/packages \
    && apt-get install -y gh bash git make ca-certificates --no-install-recommends \
    && python3 -m pip install bump2version \
    && update-ca-certificates \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* 
