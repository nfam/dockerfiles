FROM alpine

ARG VERSION="3.4.1"
LABEL build_version="freegeop version: ${VERSION}"

WORKDIR /
RUN set -xe && \
    apk add --no-cache tar wget && \
    wget -N --no-check-certificate https://github.com/fiorix/freegeoip/releases/download/v${VERSION}/freegeoip-${VERSION}-linux-amd64.tar.gz && \
    tar -xvzf freegeoip-${VERSION}-linux-amd64.tar.gz && \
    chmod +x freegeoip-${VERSION}-linux-amd64/freegeoip

FROM scratch
COPY --from=0 /freegeoip-${VERSION}-linux-amd64 /
COPY copiable /public
CMD ["/freegeoip", "-use-x-forwarded-for", "-public", "/public"]
