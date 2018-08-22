FROM outstand/ruby-base:2.4.4
MAINTAINER Ryan Schlesinger <ryan@outstand.com>

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
    apt-get install -y --no-install-recommends \
      nodejs \
      libicu-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
