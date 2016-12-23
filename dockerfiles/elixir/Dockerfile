# Image Name: elixir
# Description: Erlang Image
# Creator: Leif Gensert / leif@leif.io

FROM leifg/erlang:19.2
MAINTAINER Leif Gensert | leif@leif.io

ENV FULL_VERSION=1.3.4
ENV DOWNLOAD_SHA256=eac16c41b88e7293a31d6ca95b5d72eaec92349a1f16846344f7b88128587e10

RUN apk --update add --virtual build-dependencies curl \
    && apk --update add --virtual run-dependencies ca-certificates \
    && curl -fSL -o elixir.zip https://github.com/elixir-lang/elixir/releases/download/v${FULL_VERSION}/Precompiled.zip \
    && echo "$DOWNLOAD_SHA256 *elixir.zip" | sha256sum -c - \
    && mkdir -p /opt/elixir-${FULL_VERSION}/ \
    && unzip elixir.zip -d /opt/elixir-${FULL_VERSION}/ \
    && rm elixir.zip \
    && apk del build-dependencies \
    && rm -rf /var/cache/apk/*



RUN ln -s /opt/elixir-${FULL_VERSION} /opt/elixir
RUN ln -s /opt/elixir/bin/elixir /usr/local/bin/elixir
RUN ln -s /opt/elixir/bin/elixirrc /usr/local/bin/elixirrc
RUN ln -s /opt/elixir/bin/mix /usr/local/bin/mix
RUN ln -s /opt/elixir/bin/iex /usr/local/bin/iex

RUN mix local.hex --force
RUN mix local.rebar --force
RUN mix hex.info

CMD ["/bin/sh"]
