# Image Name: elixir
# Description: Erlang Image
# Creator: Leif Gensert / leif@leif.io

FROM leifg/erlang
MAINTAINER Leif Gensert | leif@leif.io

ENV FULL_VERSION=1.3.4
ENV DOWNLOAD_SHA256=eac16c41b88e7293a31d6ca95b5d72eaec92349a1f16846344f7b88128587e10

RUN apk --update add --virtual build-dependencies curl ca-certificates \
    && curl -fSL -o elixir.zip https://github.com/elixir-lang/elixir/releases/download/v${FULL_VERSION}/Precompiled.zip \
    && echo "$DOWNLOAD_SHA256 *elixir.zip" | sha256sum -c - \
    && mkdir -p /opt/elixir-${FULL_VERSION}/ \
    && unzip elixir.zip -d /opt/elixir-${FULL_VERSION}/ \
    && rm elixir.zip \
    && apk del build-dependencies \
    && rm -rf /etc/ssl \
    && rm -rf /var/cache/apk/*

ENV PATH $PATH:/opt/elixir-${FULL_VERSION}/bin

CMD ["/bin/sh"]
