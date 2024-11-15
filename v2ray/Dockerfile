FROM alpine
LABEL maintainer="pch18.cn"

RUN apk add --no-cache \
    caddy \
    v2ray \
    coreutils \
    util-linux \
    --repository=http://dl-cdn.alpinelinux.org/alpine/edge/testing

ENV PROTOCOL=http
ENV DOMAIN=ray.domain.com

ENV PATH_RAY=/_ray
ENV PATH_DOC=/_doc
ENV URL_DISGUISE=https://agargame.io
ENV URL_START_FILE=https://raw.githubusercontent.com/fangdajiang/dockerfiles/refs/heads/master/v2ray/start.sh
ENV ALTER_ID=0

ENV UUID_default=00000000-0000-0000-0000-000000000000

VOLUME /root/.local
CMD wget -O - ${URL_START_FILE} | sh
