ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version

USER root
RUN curl -O --silent --location https://cache.ruby-lang.org/pub/ruby/2.7/ruby-${lang_version}.tar.gz  && \
    mkdir -p /usr/local/ruby && \
    tar -zxf ruby-${lang_version}.tar.gz -C /usr/local/ruby --strip 1 && \
    rm -f ruby-${lang_version}.tar.gz && \
    ruby --version

USER jenkins
ENV PATH="$PATH:/usr/local/ruby/bin"
RUN ruby --version
