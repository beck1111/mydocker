FROM php:7.2-apache-stretch
RUN apt-get update \
    && apt-get install -y vim cron libpng-dev mysql-client \
    && docker-php-ext-install opcache mbstring zip mysqli pdo_mysql gd \
    && apt-get clean \
    && mkdir /var/log/php && chmod 777 /var/log/php \
    && a2enmod rewrite
#composer install
RUN curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer
#xdebug install
RUN pecl install xdebug \
    && docker-php-ext-enable xdebug