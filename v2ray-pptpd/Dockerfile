FROM alpine
MAINTAINER pch18.cn

RUN apk add --no-cache iptables ppp pptpd

COPY etc /etc

EXPOSE 1723

CMD set -xe \
    && iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE \
    && pptpd \
    && syslogd -n -O /dev/stdout