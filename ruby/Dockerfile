ARG base_image
FROM $base_image
MAINTAINER Jason Kulatunga <jason@thesparktree.com>
ARG lang_version

USER root
RUN apt-get update && apt-get install --no-install-recommends --yes ruby-full

USER jenkins
ENV PATH="$PATH:/usr/local/ruby/bin"
RUN ruby --version
