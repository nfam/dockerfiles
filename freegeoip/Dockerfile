FROM alpine
WORKDIR /
RUN set -xe && \
    apk add --no-cache tar wget && \
    wget -N --no-check-certificate https://github.com/fiorix/freegeoip/releases/download/v3.4.1/freegeoip-3.4.1-linux-amd64.tar.gz && \
    tar -xvzf freegeoip-3.4.1-linux-amd64.tar.gz && \
    chmod +x freegeoip-3.4.1-linux-amd64/freegeoip

FROM scratch
COPY --from=0 /freegeoip-3.4.1-linux-amd64 /
COPY copiable /public
CMD ["/freegeoip", "-use-x-forwarded-for", "-public", "/public"]
