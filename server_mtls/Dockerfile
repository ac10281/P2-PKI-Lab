FROM nginx:alpine

ENV EASYRSA_BATCH=1
ENV EASYRSA_PKI=/etc/easy-rsa/pki
ENV EASYRSA_REQ_CN=server_mtls
ENV EASYRSA_ALGO=ec
ENV EASYRSA_CURVE=secp384r1

RUN apk update && \
    apk add --no-cache easy-rsa

COPY index.html /usr/share/nginx/html/index.html
COPY default.conf /etc/nginx/conf.d/


RUN mkdir -p /etc/easy-rsa \
    && cp -r /usr/share/easy-rsa/* /etc/easy-rsa/

WORKDIR /etc/easy-rsa