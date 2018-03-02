FROM alpine
MAINTAINER Ninh Pham <ninhpham@hotmail.com>

RUN apk update \
    && apk add --no-cache --update aria2 \
    && rm -rf /var/cache/apk/*

EXPOSE 6800

ENTRYPOINT [ "/usr/bin/aria2c" ]