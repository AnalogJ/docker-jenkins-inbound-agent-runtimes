ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version
ARG build_date
ARG vcs_ref
LABEL org.label-schema.build-date=$build_date \
      org.label-schema.name="jenkins-inbound-agent-node" \
      org.label-schema.description="Jenkins inbound agent for Node" \
      org.label-schema.url="https://github.com/jenkinsci/docker-inbound-agent" \
      org.label-schema.vcs-ref=$vcs_ref \
      org.label-schema.vcs-url="https://github.com/jenkinsci/docker-inbound-agent" \
      org.label-schema.vendor="Jason Kulatunga" \
      org.label-schema.schema-version="1.0"

USER root
RUN curl -O --silent --location https://nodejs.org/dist/v${lang_version}/node-v${lang_version}-linux-x64.tar.xz  && \
    mkdir -p /usr/local/nodejs && \
    tar -xJvf node-v${lang_version}-linux-x64.tar.xz -C /usr/local/nodejs --strip 1  && \
    rm -f node-v${lang_version}-linux-x64.tar.xz
ENV PATH="$PATH:/usr/local/nodejs/bin"
RUN node --version && npm --version

USER jenkins
