# Image Name: erlang
# Description: Erlang Image
# Creator: Leif Gensert / leif@leif.io

FROM alpine:3.4
MAINTAINER Leif Gensert | leif@leif.io

ENV FULL_VERSION=19.0.1-r0

LABEL name="erlang" version=$FULL_VERSION

RUN apk --update --no-cache --repository http://nl.alpinelinux.org/alpine/edge/community add \
    git \
    erlang=$FULL_VERSION \
    erlang-dev=$FULL_VERSION \
    erlang-kernel=$FULL_VERSION \
    erlang-hipe=$FULL_VERSION \
    erlang-compiler=$FULL_VERSION \
    erlang-stdlib=$FULL_VERSION \
    erlang-erts=$FULL_VERSION \
    erlang-tools=$FULL_VERSION \
    erlang-syntax-tools=$FULL_VERSION \
    erlang-sasl=$FULL_VERSION \
    erlang-crypto=$FULL_VERSION \
    erlang-public-key=$FULL_VERSION \
    erlang-ssl=$FULL_VERSION \
    erlang-ssh=$FULL_VERSION \
    erlang-asn1=$FULL_VERSION \
    erlang-inets=$FULL_VERSION \
    erlang-mnesia=$FULL_VERSION \
    erlang-odbc=$FULL_VERSION \
    erlang-erl-interface=$FULL_VERSION \
    erlang-parsetools=$FULL_VERSION \
    erlang-eunit=$FULL_VERSION
