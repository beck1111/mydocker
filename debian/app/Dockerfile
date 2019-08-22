FROM php:7.2-fpm-stretch
RUN apt-get update \
    && docker-php-ext-install mysqli \
    && docker-php-ext-install pdo_mysql \
    && apt-get install -y vim \
    && mkdir /var/log/php && chmod 777 /var/log/php \
    && apt-get clean
COPY ./config/php.ini /usr/local/etc/php/
ADD ./config/bashrc.txt /root/.bashrc