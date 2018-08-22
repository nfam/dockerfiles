FROM alpine
LABEL maintainer="ninhpham@hotmail.com"

RUN apk add --no-cache --update avahi && \
    sed -i 's/#enable-dbus=yes/enable-dbus=no/g' /etc/avahi/avahi-daemon.conf && \
    rm -rf /var/cache/apk/*

EXPOSE 5353/udp

ENTRYPOINT ["avahi-daemon"]
CMD []