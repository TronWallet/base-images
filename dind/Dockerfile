FROM docker:stable-dind

RUN apk --update --no-cache add make git py-pip gcc python2-dev musl-dev libffi-dev openssl-dev bash \
    && pip install --no-cache-dir --upgrade pip \
    && pip install --no-cache-dir docker-compose
