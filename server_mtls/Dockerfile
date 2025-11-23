FROM nginx:alpine

RUN apk update && \
    apk add --no-cache easy-rsa

COPY index.html /usr/share/nginx/html/index.html

WORKDIR /etc/easy-rsa