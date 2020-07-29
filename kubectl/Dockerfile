FROM alpine:3.10

RUN apk update \
    && apk -U upgrade \
    && apk add --no-cache curl gettext ca-certificates make bash git \
    && update-ca-certificates --fresh \
    && rm -rf /var/cache/apk/*

# Install kubectl
RUN curl -L -o /usr/bin/kubectl https://storage.googleapis.com/kubernetes-release/release/v1.14.10/bin/linux/amd64/kubectl \
    && chmod +x /usr/bin/kubectl \
    && kubectl version --client

# install kustomize
RUN curl -s "https://raw.githubusercontent.com/kubernetes-sigs/kustomize/master/hack/install_kustomize.sh" | bash \
    && mv kustomize /usr/bin/ \
    && chmod +x /usr/bin/kustomize \
    && kustomize version
