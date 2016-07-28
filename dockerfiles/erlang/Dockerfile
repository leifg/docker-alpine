# Image Name: erlang
# Description: Erlang Image
# Creator: Leif Gensert / leif@leif.io

FROM alpine:3.4
MAINTAINER Leif Gensert | leif@leif.io

ENV ERLANG_VERSION=19.0.1-r0

LABEL name="erlang" version=$ERLANG_VERSION
RUN apk add "erlang=$ERLANG_VERSION" --no-cache --repository http://nl.alpinelinux.org/alpine/edge/community
