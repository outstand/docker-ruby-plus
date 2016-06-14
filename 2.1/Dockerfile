FROM outstand/ruby-base:2.1.9
MAINTAINER Ryan Schlesinger <ryan@outstand.com>

RUN apt-get update && apt-get install -y --no-install-recommends \
    nodejs \
    mysql-client \
    redis-tools \
  && rm -rf /var/lib/apt/lists/*

