## Simple nginx dockerfile
FROM ubuntu:latest
LABEL maintainer="Fatemeh taremi <fatemehtaremi.holm@gmail.com>"
RUN apt update \
    && apt install -y vim nginx

# forward request and error logs to docker log collector
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    && ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
