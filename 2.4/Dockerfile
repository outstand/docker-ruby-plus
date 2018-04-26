FROM outstand/ruby-base:2.4.4
MAINTAINER Ryan Schlesinger <ryan@outstand.com>

RUN apt-get update && apt-get install -y --no-install-recommends \
      nodejs \
      libicu-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
