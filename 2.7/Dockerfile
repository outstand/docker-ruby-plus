FROM outstand/ruby-base:2.7.6
LABEL maintainer="Ryan Schlesinger <ryan@outstand.com>"

SHELL ["/bin/bash", "-o", "pipefail", "-c"]
ENV DEBIAN_FRONTEND=noninteractive

RUN set -eux; \
      \
      curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | tee /usr/share/keyrings/yarnkey.gpg >/dev/null; \
      echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian stable main" | tee /etc/apt/sources.list.d/yarn.list; \
      curl -sL https://deb.nodesource.com/setup_16.x | bash -; \
      apt-get install -y --no-install-recommends \
        nodejs \
        yarn \
        libicu-dev \
      ; \
      apt-get clean; \
      rm -rf /var/lib/apt/lists/*
