FROM eu.gcr.io/kyma-project/prow/test-infra/buildpack-golang:v20181204-a6e79be

ENV HELM_VERSION="v2.10.0"

RUN wget -q https://storage.googleapis.com/kubernetes-helm/helm-${HELM_VERSION}-linux-amd64.tar.gz -O - | tar -xzO linux-amd64/helm > /usr/local/bin/helm \
    && chmod +x /usr/local/bin/helm

RUN helm init --client-only