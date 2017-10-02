FROM outstand/ruby-base:2.4.2-alpine
MAINTAINER Ryan Schlesinger <ryan@outstand.com>

ENV TMUX_VERSION 2.5

RUN apk add --no-cache \
    nodejs \
    libevent \
    ncurses-terminfo && \
  apk --no-cache add --virtual build-dependencies build-base libevent-dev ncurses-dev bsd-compat-headers && \
  mkdir -p /tmp/build && \
  cd /tmp/build && \
  wget https://github.com/tmux/tmux/releases/download/${TMUX_VERSION}/tmux-${TMUX_VERSION}.tar.gz && \
  tar -zxvf tmux-${TMUX_VERSION}.tar.gz && \
  cd tmux-${TMUX_VERSION} && \
  ./configure && make && make install && \
  cd /tmp && \
  rm -rf /tmp/build && \
  apk del build-dependencies
