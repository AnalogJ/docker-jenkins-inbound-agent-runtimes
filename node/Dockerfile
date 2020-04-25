ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version

USER root
RUN curl -O --silent --location https://nodejs.org/dist/v${lang_version}/node-v${lang_version}-linux-x64.tar.xz  && \
    tar -xJvf node-v${lang_version}-linux-x64.tar.xz -C /usr/local/nodejs --strip 1  && \
    rm -f node-v${lang_version}-linux-x64.tar.xz

USER jenkins
ENV PATH="$PATH:/usr/local/nodejs/bin"
