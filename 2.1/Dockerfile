FROM outstand/ruby-base:2.1.10
MAINTAINER Ryan Schlesinger <ryan@outstand.com>

# tmux 2.2's utf-8 support is _interesting_ in the current docker terminal code
ENV TMUX_VERSION 2.1

RUN apt-get update && apt-get install -y --no-install-recommends \
    nodejs \
  && rm -rf /var/lib/apt/lists/* && \
  mkdir -p /tmp/build && \
  cd /tmp/build && \
  wget https://github.com/tmux/tmux/releases/download/${TMUX_VERSION}/tmux-${TMUX_VERSION}.tar.gz && \
  tar -zxvf tmux-${TMUX_VERSION}.tar.gz && \
  cd tmux-${TMUX_VERSION} && \
  ./configure && make && make install && \
  cd /tmp && \
  rm -rf /tmp/build

