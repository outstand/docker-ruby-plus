FROM outstand/yarn as yarn

FROM outstand/ruby-base:2.4.9
LABEL maintainer="Ryan Schlesinger <ryan@outstand.com>"

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash - && \
    apt-get install -y --no-install-recommends \
      nodejs \
      libicu-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

COPY --from=yarn /bin/yarn /bin/
