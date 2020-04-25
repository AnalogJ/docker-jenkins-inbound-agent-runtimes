ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version

USER root
RUN apt-get update \
    && apt-get install -y \
    build-essential \
    ca-certificates \
    python${lang_version}

USER jenkins
RUN python --version
