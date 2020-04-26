ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version
ARG build_date
ARG vcs_ref
LABEL org.label-schema.build-date=$build_date \
      org.label-schema.name="jenkins-inbound-agent-go" \
      org.label-schema.description="Jenkins inbound agent for Go" \
      org.label-schema.url="https://github.com/jenkinsci/docker-inbound-agent" \
      org.label-schema.vcs-ref=$vcs_ref \
      org.label-schema.vcs-url="https://github.com/jenkinsci/docker-inbound-agent" \
      org.label-schema.vendor="Jason Kulatunga" \
      org.label-schema.schema-version="1.0"

USER root

RUN curl -O --silent --location https://dl.google.com/go/go${lang_version}.linux-amd64.tar.gz && \
    mkdir -p /usr/local/go && \
    tar -xvf go${lang_version}.linux-amd64.tar.gz -C /usr/local/go --strip 1 && \
    rm -f go${lang_version}.linux-amd64.tar.gz

USER jenkins

ENV GOROOT="/usr/local/go" \
    GOPATH="/home/jenkins/go"
ENV PATH="$GOROOT/bin:$GOPATH/bin:$PATH:/usr/local/go/bin"
RUN mkdir /home/jenkins/go && \
    go version
