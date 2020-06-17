FROM alpine:3.10

ARG GCLOUD_VERSION=296.0.0
ARG KUBECTL_VERSION=1.14.10

RUN apk update \
    && apk add --no-cache curl gettext ca-certificates make bash git python3 \
    && update-ca-certificates --fresh \
    && rm -rf /var/cache/apk/*

# Install kubectl
RUN curl -L -o /usr/bin/kubectl https://storage.googleapis.com/kubernetes-release/release/v${KUBECTL_VERSION}/bin/linux/amd64/kubectl \
    && chmod +x /usr/bin/kubectl \
    && kubectl version --client

# install kustomize
RUN curl -s "https://raw.githubusercontent.com/kubernetes-sigs/kustomize/master/hack/install_kustomize.sh" | bash \
    && mv kustomize /usr/bin/ \
    && chmod +x /usr/bin/kustomize \
    && kustomize version

# install gcloud
ENV PATH=$PATH:/opt/google-cloud-sdk/bin
RUN curl -LO "https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-${GCLOUD_VERSION}-linux-x86_64.tar.gz" \
    && tar -xzvf google-cloud-sdk-${GCLOUD_VERSION}-linux-x86_64.tar.gz \
    && rm -f google-cloud-sdk-${GCLOUD_VERSION}-linux-x86_64.tar.gz \
    && mv google-cloud-sdk /opt/ \
    && gcloud version

