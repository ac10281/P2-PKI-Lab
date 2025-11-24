FROM nginx:alpine

RUN apk update && \
    apk add --no-cache openssl easy-rsa

COPY index.html /usr/share/nginx/html/index.html
COPY default.conf /etc/nginx/conf.d/

EXPOSE 443