ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version
ARG build_date
ARG vcs_ref
LABEL org.label-schema.build-date=$build_date \
      org.label-schema.name="jenkins-inbound-agent-ruby" \
      org.label-schema.description="Jenkins inbound agent for Ruby" \
      org.label-schema.url="https://github.com/jenkinsci/docker-inbound-agent" \
      org.label-schema.vcs-ref=$vcs_ref \
      org.label-schema.vcs-url="https://github.com/jenkinsci/docker-inbound-agent" \
      org.label-schema.vendor="Jason Kulatunga" \
      org.label-schema.schema-version="1.0"

USER root
RUN apt-get update && apt-get install --no-install-recommends --yes ruby-full

USER jenkins
ENV PATH="$PATH:/usr/local/ruby/bin"
RUN ruby --version
