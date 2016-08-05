# Image Name: elixir
# Description: Erlang Image
# Creator: Leif Gensert / leif@leif.io

FROM leifg/erlang
MAINTAINER Leif Gensert | leif@leif.io

ENV FULL_VERSION 1.3.2
ENV DOWNLOAD_SHA256 45fdb9464b0fbe44c919482f1247740cc9c5d399280ef07e386aa7402b085be7

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
