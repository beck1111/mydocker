FROM php:7.2-fpm-alpine
COPY ./config/php.ini /usr/local/etc/php/
RUN docker-php-ext-install mysqli \
    && docker-php-ext-install pdo_mysql \
    && apk update \
    && apk add vim \
    && source /root/.ashrc \
    && mkdir /var/log/php && chmod 777 /var/log/php
ADD ./config/bashrc.txt /root/.ashrc