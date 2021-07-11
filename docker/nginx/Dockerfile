FROM nginx:stable-alpine

ADD docker/nginx/conf/nginx.conf /etc/nginx/nginx.conf
ADD docker/nginx/conf/default.conf /etc/nginx/conf.d/default.conf

RUN mkdir -p /var/www/html

RUN addgroup -g 1000 user_app && adduser -G user_app -g user_app -s /bin/sh -D user_app

RUN chown user_app:user_app /var/www/html