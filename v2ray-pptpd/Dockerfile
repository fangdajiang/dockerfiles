FROM alpine
MAINTAINER pch18.cn

RUN apk add --no-cache iptables ppp pptpd \
    && wget https://github.com/v2fly/v2ray-core/releases/download/v5.1.0/v2ray-linux-64.zip \
    

COPY etc /etc

EXPOSE 1723

CMD set -xe \
    && iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE \
    && pptpd \
    && syslogd -n -O /dev/stdout