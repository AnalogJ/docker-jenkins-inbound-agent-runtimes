ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version

USER root

RUN curl -O --silent --location https://dl.google.com/go/go${lang_version}.linux-amd64.tar.gz && \
    tar -xvf go${lang_version}.linux-amd64.tar.gz -C /usr/local && \
    rm -f go${lang_version}.linux-amd64.tar.gz && \
    go --version

USER jenkins

ENV GOROOT="/usr/local/go" \
    GOPATH="/home/jenkins/go"
ENV PATH="$GOROOT/bin:$GOPATH/bin:$PATH"
RUN mkdir /home/jenkins/go
