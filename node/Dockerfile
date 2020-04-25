ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version

USER root
RUN curl -O --silent --location https://nodejs.org/dist/v${lang_version}/node-v${lang_version}-linux-x64.tar.xz  && \
    tar -zxf node-v${lang_version}-linux-x64.tar.xz -C /usr/local && \
    mv go /usr/local && \
    rm -f node-v${lang_version}-linux-x64.tar.xz && \
    node -v && \
    npm version

USER jenkins
