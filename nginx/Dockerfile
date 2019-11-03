FROM nginx:1.15.0-alpine
RUN apk update && apk add bash

RUN rm /etc/nginx/conf.d/default.conf
COPY ./vhost.conf /etc/nginx/conf.d
COPY ./vhost2.conf /etc/nginx/conf.d
