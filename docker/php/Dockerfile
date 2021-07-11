FROM php:8.0.8-fpm-alpine3.14

ADD docker/php/conf /etc/php/8.0/cli/
RUN addgroup -g 1000 user_app && adduser -G user_app -g user_app -s /bin/sh -D user_app

RUN mkdir -p /var/www/html

RUN chown user_app:user_app /var/www/html

WORKDIR /var/www/html

RUN apk add --no-cache $PHPIZE_DEPS && pecl install xdebug-2.9.7 && docker-php-ext-enable xdebug

RUN apk add --update --no-cache libintl icu icu-dev libxml2-dev && docker-php-ext-configure intl

RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.6/community' >> /etc/apk/repositories
RUN apk update && \
  apk add --no-cache 'tidyhtml-dev==5.2.0-r1'

RUN docker-php-ext-install -j$(nproc) tidy

COPY docker/php/conf/php.ini /usr/local/etc/php/php.ini
COPY docker/php/conf/docker-xdebug.ini /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

RUN docker-php-ext-install intl pdo pdo_mysql