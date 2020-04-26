ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version
ARG build_date
ARG vcs_ref
LABEL org.label-schema.build-date=$build_date \
      org.label-schema.name="jenkins-inbound-agent-python" \
      org.label-schema.description="Jenkins inbound agent for Python" \
      org.label-schema.url="https://github.com/jenkinsci/docker-inbound-agent" \
      org.label-schema.vcs-ref=$vcs_ref \
      org.label-schema.vcs-url="https://github.com/jenkinsci/docker-inbound-agent" \
      org.label-schema.vendor="Jason Kulatunga" \
      org.label-schema.schema-version="1.0"

USER root
RUN apt-get update \
    && apt-get install -y \
    build-essential \
    ca-certificates \
    python${lang_version}

USER jenkins
RUN python --version
