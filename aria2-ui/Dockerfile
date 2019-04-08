FROM nginx:alpine
LABEL maintainer="ninhpham@hotmail.com"

ARG VERSION="1.0.2"
LABEL build_version="AriaNg version: ${VERSION}"

RUN set -xe && \
    apk add --no-cache unzip wget && \
    wget -N --no-check-certificate https://github.com/mayswind/AriaNg/releases/download/${VERSION}/AriaNg-${VERSION}.zip && \
    unzip -o AriaNg-${VERSION}.zip -d /usr/share/nginx/html && \
    rm -rf AriaNg-${VERSION}.zip && \
    apk del unzip wget
