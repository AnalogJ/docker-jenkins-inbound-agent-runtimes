ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version

USER root
RUN curl -O --silent --location https://rubies.travis-ci.org/ubuntu/16.04/ppc64le/ruby-${lang_version}.tar.bz2 && \
    mkdir -p /usr/local/ruby && \
    tar -xvf ruby-${lang_version}.tar.bz2 -C /usr/local/ruby --strip 1 && \
    rm -f ruby-${lang_version}.tar.bz2

USER jenkins
ENV PATH="$PATH:/usr/local/ruby/bin"
RUN ruby --version
