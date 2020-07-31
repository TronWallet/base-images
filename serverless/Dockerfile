FROM node:10.16.0-buster

RUN curl -lO  https://storage.googleapis.com/golang/go1.14.6.linux-amd64.tar.gz \
&& tar -C /usr/local -xzf go1.14.6.linux-amd64.tar.gz

RUN apt update && apt install -y less

RUN yarn global add serverless
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
&& unzip awscliv2.zip \
&& ./aws/install

ENV PATH="/usr/local/go/bin:${PATH}"