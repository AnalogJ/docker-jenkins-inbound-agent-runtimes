ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version

USER root
RUN curl -O --silent --location https://cache.ruby-lang.org/pub/ruby/2.7/ruby-${lang_version}.tar.gz  && \
    mkdir -p /usr/src/ruby && \
    tar -zxf ruby-${lang_version}.tar.gz -C /usr/src/ruby --strip 1 && \
    rm -f ruby-${lang_version}.tar.gz && \
    cd  /usr/src/ruby && \
    ./configure --disable-install-doc --enable-shared && \
    make install && \
    rm -rf /usr/src/ruby && \
    ruby --version && \
    gem --version && \
    bundle --version

ENV GEM_HOME=/usr/local/bundle
ENV BUNDLE_SILENCE_ROOT_WARNING=1 \
	BUNDLE_APP_CONFIG="$GEM_HOME"
ENV PATH="$PATH:/usr/local/ruby/bin"
# adjust permissions of a few directories for running "gem install" as an arbitrary user
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"


USER jenkins
